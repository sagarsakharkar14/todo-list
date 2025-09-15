🔗 URL Configuration – To-Do List App (DRF)
This section outlines the backend routes for your Django REST Framework–based To-Do List application. 

Endpoint Reference

urlpatterns = [
    path('login/', CustomLoginView.as_view(), name='login'),
    path('logout/', LogoutView.as_view(next_page='login/'), name='logout'),
    path('', TaskList.as_view(), name='tasks'),
    path('task/<int:pk>/', TaskDetail.as_view(), name='task'),
    path('task-create/', TaskCreate.as_view(), name='task-create'),
    path('task-update/<int:pk>/', TaskUpdate.as_view(), name='task-update'),
    path('task-delete/<int:pk>/', TaskDelete.as_view(), name='task-delete'),
]


| /login/ |  | CustomLoginView |  | 
| /logout/ |  | LogoutView |  | 
| / |  | TaskList |  | 
| /task/<int:pk>/ |  | TaskDetail |  | 
| /task-create/ |  | TaskCreate |  | 
| /task-update/<int:pk>/ |  | TaskUpdate |  | 
| /task-delete/<int:pk>/ |  | TaskDelete |  | 

- User Registration & Login
- Create, Read, Update, Delete Tasks
- Mark tasks as complete/incomplete

pip install -r requirements.txt
python manage.py migrate
python manage.py runserver


