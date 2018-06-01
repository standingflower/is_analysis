<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setOneStudentResults  [返回](../README.md)
用例： [评定成绩](../用例/评定成绩.md)

- 功能：
    对同学的某一实验进行评定成绩和评语
    
    输入参数result不为空，自动设置update_date为当前日期，表示同时设置批改日期。
    
    输入参数result为空，自动设置update_date为空，表示未批改。
    
- 权限：
    老师：可以查看所有学生的成绩。
    
- API请求地址： 
    接口基本地址/v1/api/etOneStudentResults

- 请求方式 ：
    POST
 
- 请求实例：  
        { 
            "student_id": "201510315203", 
            "test_id": "10201",
            "course_id":"04470580",
            "data": [
                {
                "result1": 40, 
                "memo1":"本实验做得好",
                }, 
                {
                "result2": 30, 
                "memo2":"本实验做得好",
                },
                {
                "result3": 30, 
                "memo3":"本实验做得好",
                }
            ] 
        }

- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学号|
  |test_id|对应实验的编号|
  |course_id|课程编号|
  |data|实验的成绩和评语|
  |result|一个实验的不同评判标准的得分|
  |memo|对实验进行评价|   
 
- 返回实例：

        {         
            "status": true,
            "info": null
        }

- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


