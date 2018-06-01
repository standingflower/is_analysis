<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getOneStudentResults  [返回](../README.md)
用例： [查看成绩](../用例/查看成绩.md)，[评定成绩](../用例/评定成绩.md)

- 功能：
    返回一个学生的实验成绩和实验评价。
    
- 权限：
    学生：只能查看自己的成绩，即接口参数student_id必须等于登录学生的student_id
    老师：可以查看所有学生的成绩。
    
- API请求地址： 
    接口基本地址/v1/api/getOneStudentResults/<student_id>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |student_id|学生的学号|
  |test_id|实验编号|
    
- 返回实例：

        {         
            "status": true,
            "info": null,    
            "student_id": "201510421131", 
            "github_username": "standingflower", 
            "class": "软件(本)15-2", 
            "name": "郑涛", 
            "result_sum":90.5,       "update_date": "2018-04-02 13:48:01"
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
            "update_date": "2018-04-02 13:48:01"
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |student_id|学号|
  |github_username|学生的gitHub用户名|
  |class|班级|
  |name|真实姓名|   
  |result_sum|实验平均成绩|   
  |result|一个实验的不同评判标准的得分|
  |memo|对实验进行评价| 
  |update_date|本实验老师的批改日期，可以为空|


