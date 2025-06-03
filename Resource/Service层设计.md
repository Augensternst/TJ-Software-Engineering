# Service层设计

## **1. 用户服务类（UserService）**  

负责用户的注册、登录和用户信息管理。

### 方法

- `registerUser(username: String, password: String, email: String, role: String): void`  
  用户注册。
- `loginUser(email: String, password: String): User`  
  用户登录并返回用户信息。
- `getUserById(userId: int): User`  
  根据用户ID获取用户信息。
- `getAllUsers(): List<User>`  
  获取所有用户信息（管理员使用）。
- `updateUserRole(userId: int, newRole: String): void`  
  修改用户角色（如由管理员授权为老师）。

---

## **2. 课程服务类（CourseService）**  

负责课程的创建和管理。

### 方法

- `createCourse(courseName: String, teacherId: int, description: String): Course`  
  创建新课程。
- `getCourseById(courseId: int): Course`  
  根据ID获取课程详情。
- `getCoursesByTeacher(teacherId: int): List<Course>`  
  获取某老师创建的所有课程。
- `assignStudentToCourse(studentId: int, courseId: int): void`  
  老师邀请学生加入课程。
- `getStudentsInCourse(courseId: int): List<User>`  
  获取课程中的学生列表。

---

## **3. 任务服务类（TaskService）**  

负责任务的布置和任务管理。

### 方法

- `createTask(courseId: int, teacherId: int, taskType: String, description: String): Task`  
  创建任务。
- `getTasksByCourse(courseId: int): List<Task>`  
  获取课程下的所有任务。
- `assignImageToTask(taskId: int, imageId: int): void`  
  关联任务和图片。
- `getTaskDetails(taskId: int): Task`  
  获取任务详情，包括关联的图片和描述。

---

## **4. 图片服务类（ImageService）**  

负责图片的上传和管理。

### 方法

- `uploadImage(imageUrl: String, description: String): Image`  、、、
  上传图片。。。。
- `getImagesByTask(taskId: int): List<Image>`  
  获取某任务的所有图片。
- `deleteImage(imageId: int): void`  
  删除指定图片。。。。、、、、、

---

## **5. 学生任务服务类（StudentTaskService）**  

负责学生提交任务和反馈管理。

### 方法

- `submitResponse(studentId: int, taskId: int, responseText: String): void`  
  学生提交任务。
- `getResponsesByTask(taskId: int): List<StudentResponse>`  
  获取某任务的所有学生提交。
- `gradeResponse(responseId: int, score: Decimal, feedback: String): void`  
  教师对学生的任务进行评分和反馈。

---

## **6. 管理员服务类（AdminService）**  

负责审核教师资质和系统管理。

### 方法

- `approveTeacher(userId: int): void`  
  审核并批准某用户为教师。
- `getPendingTeacherRequests(): List<User>`  
  获取待审核的教师列表。
- `viewUserInfo(userId: int): User`  
  查看用户信息。
- `removeUser(userId: int): void`  
  移除用户。

---

## **类之间的依赖关系**

- **UserService** 会与 **CourseService** 和 **AdminService** 交互，因为用户可以是学生或教师，管理员需要处理用户的审核。  
- **CourseService** 会调用 **UserService** 获取教师和学生的信息，并调用 **TaskService** 来创建课程相关的任务。  
- **TaskService** 和 **ImageService** 会协作管理任务的图片资源。  
- **StudentTaskService** 用于处理学生的任务提交，评分时会与 **TaskService** 协作。

---

### **类图示例**（伪代码）

```text
UserService --- CourseService --- TaskService --- ImageService
                      |                 |
                      |                 v
             StudentTaskService    AdminService
```
