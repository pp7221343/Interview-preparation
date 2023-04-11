
# mysql case 判断null

## 错误写法

* case value when value is null then value else value2 end

## 正确写法

* **case when** value is null then value else value2 end


# mysql not in 参数中有null返回值错误解决办法

* select * from test where feild in ();

## 取反错误写法
* select * from test where feild not in ();

## 正确写法
* select * from test where feild in () is not TRUE;







    
    
