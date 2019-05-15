# Database Modeling

* 3NF를 위배하는사항
  > 프라이머리 키를 제외하고 장르이름에 장르약어가 종속되어 있으므로 3NF를 위배한다.

+
```java
package com.cafe24.bookmall.dao;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;
import java.util.ArrayList;
import java.util.List;

import com.cafe24.bookmall.vo.CartVo;
import com.cafe24.bookmall.vo.OrderBookVo;

public class OrderBookDao extends DBConnection {
	public boolean insert(OrderBookVo vo) {

		boolean result = false;

		Connection conn = null;
		PreparedStatement pstmt = null;
		try {
			conn= getConnection();
			String sql = "insert into order_book values(?,?,?,?)";
			pstmt = conn.prepareStatement(sql);

			pstmt.setLong(1, vo.getOrderNo());
			pstmt.setLong(2, vo.getBookNo());
			pstmt.setLong(3, vo.getCount());
			pstmt.setLong(4, vo.getPrice());
			int count = pstmt.executeUpdate();

			result = (count==1);
		} catch (ClassNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (SQLException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}finally {
			try {
				if(pstmt != null)
					pstmt.close();
				if(conn!=null)
					conn.close();
			}catch(SQLException e) {
				e.printStackTrace();
			}
		}
		return result;
	}
	public List<OrderBookVo> getList(){
		List<OrderBookVo> list = new ArrayList <OrderBookVo>();

		Connection conn = null;
		PreparedStatement pstmt = null;
		ResultSet rs = null;
		try {
			conn = getConnection();
			String sql = "select *\r\n" +
					" from order_book";
			pstmt = conn.prepareStatement(sql);
			rs = pstmt.executeQuery();

			while(rs.next() == true) {
				Long orderNo = rs.getLong(1);
				Long bookNo  = rs.getLong(2);
				Long count   = rs.getLong(3);
				Long price   = rs.getLong(4);
				OrderBookVo vo= new OrderBookVo();

				vo.setOrderNo(orderNo);
				vo.setBookNo(bookNo);
				vo.setCount(count);
				vo.setPrice(price);

				list.add(vo);
			}
		} catch (ClassNotFoundException e) {
			System.out.println("Driver loading fail : "+e);
		} catch (SQLException e) {
			System.out.println("error "+e);
		} finally {
			//자원정리(Clean-Up)
			try {
				if(pstmt != null) {
					pstmt.close();
				}
				if(rs != null) {
					rs.close();
				}
				if(conn != null)
					conn.close();
			} catch (SQLException e) {
				e.printStackTrace();
			}
		}
		return list;
	}
  ```

}
