# todo-api
API tests for todo app (Java)


Firstly, you need to run Flask server with todo app on your localhost:5000:
./app.py

To authorize you need to add to curl command:
-u miguel:python

To clear task_list:
curl -u miguel:python -i -H "Content-Type: application/json" -X PUT http://localhost:5000/todo/api/v1.0/tasks

To get tasks:
curl -u miguel:python -i http://localhost:5000/todo/api/v1.0/tasks

To create task:
curl -i -H "Content-Type: application/json" -X POST -d '{"title":"add_your_title"}' http://localhost:5000/todo/api/v1.0/tasks

To update task[id]:
curl -i -H "Content-Type: application/json" -X PUT -d '{"done":true}' http://localhost:5000/todo/api/v1.0/tasks/2

To delete task[id]:
curl -i -H "Content-Type: application/json" -X DELETE http://localhost:5000/todo/api/v1.0/tasks/2
