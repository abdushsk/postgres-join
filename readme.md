# SQL Practice Questions Repository

## Introduction

This repository contains a curated collection of SQL questions designed to enhance your skills in:

- Complex joins
- Aggregations with `GROUP BY`
- Filtering with `WHERE` and `HAVING`
- Self-joins and conditional logic
- Real-world database querying

The dataset includes tables such as `students`, `courses`, `enrollments`, `majors`, `professors`, and `departments`.


## Schema

### Departments Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| department_id    | INT     | Primary key for the departments.      |
| department_name  | VARCHAR | Name of the department.               |

### Majors Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| major_id         | INT     | Primary key for the majors.           |
| major_name       | VARCHAR | Name of the major.                    |
| department_id    | INT     | Foreign key referencing Departments.  |

### Students Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| student_id       | INT     | Primary key for the students.         |
| name             | VARCHAR | Name of the student.                  |
| email            | VARCHAR | Email of the student.                 |
| age              | INT     | Age of the student.                   |
| major_id         | INT     | Foreign key referencing Majors.       |

### Professors Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| professor_id     | INT     | Primary key for the professors.       |
| professor_name   | VARCHAR | Name of the professor.                |
| professor_email  | VARCHAR | Email of the professor.               |
| department_id    | INT     | Foreign key referencing Departments.  |

### Courses Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| course_id        | INT     | Primary key for the courses.          |
| course_name      | VARCHAR | Name of the course.                   |
| credits          | INT     | Number of credits for the course.     |
| department_id    | INT     | Foreign key referencing Departments.  |

### Enrollments Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| enrollment_id    | INT     | Primary key for the enrollments.      |
| student_id       | INT     | Foreign key referencing Students.     |
| course_id        | INT     | Foreign key referencing Courses.      |
| grade            | CHAR    | Grade of the student in the course.   |

### Department_Head Table
| Column           | Type    | Description                           |
|------------------|---------|---------------------------------------|
| department_id    | INT     | Foreign key referencing Departments.  |
| professor_id     | INT     | Foreign key referencing Professors.   |

## How to Use

1. Clone the repository to your local machine.
2. Import the dataset into your SQL client (e.g., PostgreSQL, MySQL).
3. Execute each query to test your understanding of SQL concepts.

## Contributing

Contributions are welcome! If you have additional questions or improvements, feel free to create a pull request or open an issue.

## License

This repository is licensed under the MIT License. See `LICENSE` for more details.