表数据：
部门  姓名  月薪
1     张三  1000
1     李四  200
2     王五  500
2     小明  1000
1     张三  200
2     张三  300


sql语句：

SELECT 部门,姓名,SUM(月薪)AS TOTAL 
FROM PERSON
GROUP BY  部门,姓名  WITH ROLLUP


查询结果：
部门  姓名  TOTAL
1     小明  400
1     张三  3001
1     李四  200
1           3601
2     小亮  600
2     小红  500
2     张三  70
2           1170
            4771
