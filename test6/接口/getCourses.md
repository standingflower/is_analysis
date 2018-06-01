<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getCourses  [返回](../README.md)
用例： [课程列表](../用例/选择课程.md)

- 功能：
    获取用户对应的所有课程信息。
    
- 权限：    
    必须登录，学生或老师。
    
- API请求地址： 
    接口基本地址/v1/api/getCourses

- 请求方式 ：
    POST

- 请求参数说明:        

  请求参数为students_id或teachers_id。
    
- 返回实例：

        {         
            	"status": true,
				"info": null,
				"total": 5,
				"data":[
					{
						"course_id":"04470580",
						"course_name":"软件系统分析与设计技术",
						"name":"赵卫东"},
					{
					...其他课程
					}
				]
        }



- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回课程总数|
  |data|所有课程的数组|
  |course_id|课程的编号|
  |course_name|课程名称|
  |name|任课老师名称|



