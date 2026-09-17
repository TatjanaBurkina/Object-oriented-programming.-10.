# 🎓 Student Group Management System (Управление студенческими группами)

Учебный Java-проект, реализующий архитектуру для создания и управления студенческими группами. Проект демонстрирует принципы проектирования сервисного слоя (Service Layer), разделения ответов модели данных (Entity) и управления через контроллер.

---

## 📂 Структура проекта

Исходный код приложения находится в корневой директории и включает следующие основные компоненты:

```text
├── Controller.java             # Главный управляющий класс (точка входа)
├── Student.java                # Сущность студента (ID и имя)
├── Teacher.java                # Сущность преподавателя (ID и имя)
├── StudentGroup.java           # Модель учебной группы (преподаватель + список студентов)
└── StudentGroupService.java    # Сервис бизнес-логики для создания групп




import java.util.List;

public class Controller {
    public static void main(String[] args) {
        Teacher teacher = new Teacher(1, "Ivan Petrov");
        
        Student s1 = new Student(101, "Maria Ivanova");
        Student s2 = new Student(102, "Alexey Smirnov");
        Student s3 = new Student(103, "Svetlana Kuznetsova");
        
        List<Student> students = List.of(s1, s2, s3);
        
        StudentGroupService service = new StudentGroupService();
        StudentGroup group = service.createGroup(teacher, students);
        
        System.out.println(group);
    }
}
