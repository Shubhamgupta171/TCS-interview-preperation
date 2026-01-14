# Top 50 TCS Digital Interview Questions and Answers

## Technical and Programming Questions

1. **What is Object-Oriented Programming (OOP)?**
   - OOP is a programming paradigm based on objects which contain data and methods. Key concepts: encapsulation, inheritance, polymorphism, abstraction.

2. **What is the difference between C and C++?**
   - C is procedural, C++ is both procedural and object-oriented. C++ supports classes, objects, inheritance, and polymorphism.

3. **What are the four pillars of OOP?**
   - Encapsulation, Abstraction, Inheritance, Polymorphism.

4. **Explain the concept of inheritance.**
   - Inheritance allows one class to inherit properties and behaviors from another class, promoting code reuse.

5. **What is polymorphism?**
   - The ability of different objects to respond uniquely to the same function call (method overloading and overriding).

6. **Difference between method overloading and overriding.**
   - Overloading: Same method name, different parameters, same class.
   - Overriding: Same method name and parameters, different classes (parent-child relationship).

7. **What is a constructor?**
   - A special method called automatically when an object is created, used to initialize objects.

8. **Difference between Stack and Queue.**
   - Stack: LIFO (Last In First Out); Queue: FIFO (First In First Out).

9. **What is a Linked List?**
   - A data structure where elements (nodes) are linked using pointers.

10. **What is recursion?**
    - A function calling itself to solve a problem.

11. **Explain the concept of normalization in databases.**
    - Organizing data to reduce redundancy and improve data integrity.

12. **What is SQL JOIN? Types?**
    - JOIN combines rows from two or more tables. Types: INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN.

13. **Difference between Primary Key and Foreign Key.**
    - Primary Key: Uniquely identifies a row. Foreign Key: References Primary Key in another table.

14. **What is the difference between an abstract class and interface in Java?**
    - Abstract class can have method implementations; interface cannot (until Java 8's default methods).

15. **Explain exception handling in Java.**
    - Mechanism to handle runtime errors using try-catch-finally blocks.

16. **What is a deadlock?**
    - A situation where two or more processes are unable to proceed because each is waiting for the other to release resources.

17. **Explain multithreading.**
    - Concurrent execution of multiple threads to maximize CPU utilization.

18. **What is the difference between process and thread?**
    - Process: Independent program in execution. Thread: Smallest unit of a process.

19. **How do you reverse a string in Java?**
    - Using StringBuilder’s reverse() method or by iterating from end to start.

    ```java
    String str = "hello";
    String reversed = new StringBuilder(str).reverse().toString();
    ```

20. **Write a program to find the factorial of a number.**
    ```java
    int factorial(int n) {
        if(n == 0) return 1;
        else return n * factorial(n-1);
    }
    ```

21. **What is a binary search?**
    - Efficient search algorithm for sorted arrays, repeatedly dividing search interval in half.

22. **Difference between Array and ArrayList in Java.**
    - Array: Fixed size, can store primitive types. ArrayList: Dynamic size, stores objects only.

23. **What is encapsulation?**
    - Wrapping data and code together as a single unit, restricting direct access.

24. **Explain the MVC architecture.**
    - Model-View-Controller separates application into three interconnected components.

25. **What are collections in Java?**
    - Framework providing architecture to store and manipulate groups of objects (List, Set, Map, etc.).

26. **Write code to check if a number is prime.**
    ```java
    boolean isPrime(int n) {
        if(n <= 1) return false;
        for(int i=2; i<=Math.sqrt(n); i++)
            if(n % i == 0) return false;
        return true;
    }
    ```

27. **What is the difference between == and .equals() in Java?**
    - == checks reference equality; .equals() checks value/content equality.

28. **What is the use of the 'final' keyword in Java?**
    - Makes variables constant, methods non-overridable, and classes non-inheritable.

29. **Explain garbage collection in Java.**
    - Automatic memory management process that reclaims memory occupied by unreferenced objects.

30. **What is normalization? Explain 1NF, 2NF, 3NF.**
    - Process of organizing data to minimize redundancy.
      - 1NF: Atomic columns.
      - 2NF: 1NF + full functional dependency.
      - 3NF: 2NF + no transitive dependency.

## Coding/Algorithmic Challenges

31. **Find the second largest number in an array.**
    ```java
    int first = Integer.MIN_VALUE, second = Integer.MIN_VALUE;
    for(int n : arr) {
        if(n > first) {
            second = first;
            first = n;
        } else if(n > second && n != first) {
            second = n;
        }
    }
    ```

32. **Write a program to print Fibonacci series.**
    ```java
    int a=0, b=1;
    for(int i=0; i<n; i++) {
        System.out.print(a + " ");
        int sum = a + b;
        a = b;
        b = sum;
    }
    ```

33. **Write a SQL query to fetch the second highest salary from a table.**
    ```sql
    SELECT MAX(salary) FROM employees WHERE salary < (SELECT MAX(salary) FROM employees);
    ```

34. **What is a palindrome? Write code to check palindrome.**
    - Word/number that reads same backward and forward.

    ```java
    boolean isPalindrome(String s) {
        int i=0, j=s.length()-1;
        while(i < j) if(s.charAt(i++) != s.charAt(j--)) return false;
        return true;
    }
    ```

35. **Swap two numbers without using a third variable.**
    ```java
    a = a + b;
    b = a - b;
    a = a - b;
    ```

36. **Write code to remove duplicates from an array.**
    ```java
    Set<Integer> set = new HashSet<>(Arrays.asList(arr));
    Integer[] unique = set.toArray(new Integer[0]);
    ```

37. **Difference between Stack Overflow and Heap Overflow.**
    - Stack Overflow: Too many nested method calls.
    - Heap Overflow: Memory allocation exceeds heap size.

38. **What is Big O notation?**
    - Describes the time/space complexity of an algorithm in worst-case scenario.

39. **What is a hash map?**
    - Data structure that maps keys to values using hash functions for fast lookup.

40. **Explain static keyword in Java.**
    - Used for class-level variables and methods, shared among all instances.

## HR & General Questions

41. **Tell me about yourself.**
    - [Prepare a brief, career-focused self-introduction highlighting your education, projects, and skills.]

42. **Why do you want to join TCS Digital?**
    - [Mention TCS' reputation, digital focus, learning opportunities, and alignment with your career goals.]

43. **Where do you see yourself in 5 years?**
    - [Express your aspiration to grow technically, take leadership roles, and contribute to company success.]

44. **What are your strengths and weaknesses?**
    - [Share strengths relevant to job, and weaknesses with mention of improvement steps.]

45. **Tell me about a challenging project you handled.**
    - [Describe the project, challenges, your approach, and impact.]

46. **Are you comfortable relocating?**
    - [Answer honestly, but flexibility is appreciated in campus interviews.]

47. **How do you handle pressure or tight deadlines?**
    - [Discuss prioritization, time management, and staying calm.]

48. **What are your hobbies?**
    - [Mention hobbies that show creativity, dedication, or teamwork.]

49. **Have you worked in a team? Describe your experience.**
    - [Share a positive teamwork experience, emphasizing collaboration and learning.]

50. **Do you have any questions for us?**
    - [Ask about training, growth opportunities, or company culture.]


# 📘 SQL Interview Questions & Answers (Quick Revision)

---

## 🟢 Basic SQL

1. **What is SQL?**
   - A language used to store, retrieve, update, and manage data in relational databases.

2. **What is DBMS?**
   - A system that allows users to define, create, and manage databases.

3. **What is RDBMS?**
   - A database system that stores data in tables with relationships using keys.

4. **What is a table?**
   - A structured collection of data organized into rows and columns.

5. **What is a primary key?**
   - A column that uniquely identifies each row and cannot be NULL.

6. **What is a foreign key?**
   - A column that creates a relationship between two tables.

7. **What is NULL in SQL?**
   - A value that represents missing or unknown data.

8. **What is the difference between DELETE and TRUNCATE?**
   - DELETE removes selected rows and can be rolled back.
   - TRUNCATE removes all rows and cannot be rolled back.

9. **What is DDL?**
   - Data Definition Language used to define database structure (CREATE, ALTER, DROP).

10. **What is DML?**
    - Data Manipulation Language used to modify data (INSERT, UPDATE, DELETE).

11. **What is DCL?**
    - Data Control Language used for access control (GRANT, REVOKE).

12. **What is TCL?**
    - Transaction Control Language used to manage transactions (COMMIT, ROLLBACK).

13. **What is a constraint?**
    - Rules applied to table columns to ensure data integrity.

14. **What is UNIQUE constraint?**
    - Ensures all values in a column are unique.

15. **Difference between CHAR and VARCHAR?**
    - CHAR uses fixed length; VARCHAR uses variable length.

---

## 🟡 Intermediate SQL

16. **What is JOIN?**
    - Used to combine data from multiple tables based on a related column.

17. **What are the types of JOINs?**
    - INNER, LEFT, RIGHT, FULL.

18. **What is INNER JOIN?**
    - Returns only matching records from both tables.

19. **What is LEFT JOIN?**
    - Returns all records from left table and matching records from right table.

20. **Difference between WHERE and HAVING?**
    - WHERE filters rows; HAVING filters grouped data.

21. **What is GROUP BY?**
    - Groups rows that have the same values in specified columns.

22. **What are aggregate functions?**
    - Functions like COUNT, SUM, AVG, MIN, MAX.

23. **What is ORDER BY?**
    - Sorts the result set in ascending or descending order.

24. **What is BETWEEN operator?**
    - Filters data within a specified range.

25. **What is LIKE operator?**
    - Used for pattern matching in queries.

26. **Difference between IN and EXISTS?**
    - IN compares values; EXISTS checks for subquery result existence.

27. **What is a subquery?**
    - A query nested inside another SQL query.

28. **What is UNION?**
    - Combines results of multiple SELECT queries and removes duplicates.

29. **Difference between UNION and UNION ALL?**
    - UNION removes duplicates; UNION ALL keeps duplicates.

30. **What is a view?**
    - A virtual table created using a SELECT query.

31. **What is an index?**
    - A database object that improves query performance.

32. **Difference between clustered and non-clustered index?**
    - Clustered index sorts data physically; non-clustered does not.

33. **What is normalization?**
    - Process of organizing data to reduce redundancy.

34. **What are normal forms?**
    - 1NF, 2NF, 3NF, BCNF.

35. **What is denormalization?**
    - Adding redundancy to improve read performance.

---

## 🔴 Advanced SQL

36. **What is a transaction?**
    - A sequence of operations performed as a single logical unit.

37. **What are ACID properties?**
    - Atomicity, Consistency, Isolation, Durability.

38. **What is an isolation level?**
    - Controls how transactions are isolated from each other.

39. **What are transaction isolation levels?**
    - Read Uncommitted, Read Committed, Repeatable Read, Serializable.

40. **What is a deadlock?**
    - When two transactions wait indefinitely for each other.

41. **What is a stored procedure?**
    - A precompiled set of SQL statements stored in the database.

42. **Difference between stored procedure and function?**
    - Functions return values; procedures may not.

43. **What is a trigger?**
    - Automatically executed SQL code on data changes.

44. **What is a cursor?**
    - Used to process rows one at a time.

45. **What is a window function?**
    - Performs calculations across a set of rows without grouping.

46. **Give an example of a window function.**
    - ROW_NUMBER(), RANK(), DENSE_RANK().

47. **What is a CTE?**
    - Common Table Expression used for readable and reusable queries.

48. **What is a self join?**
    - A table joined with itself.

49. **What is database locking?**
    - Mechanism to control concurrent access to data.

50. **Difference between SQL and NoSQL?**
    - SQL uses structured schema; NoSQL uses flexible schema.

---


# 📘 Backend & System Design Interview Questions (With Examples)

---

## 🟢 Backend Fundamentals

1. **What is Backend Development?**
   - Backend handles business logic, database operations, authentication, and APIs.
   - Example: Login validation, storing user data, generating reports.

2. **What is Client–Server Architecture?**
   - Client sends requests, server processes them and sends responses.
   - Example: Browser (client) → API (server) → Database → Response.

3. **What is an API?**
   - API is a contract that allows two systems to communicate.
   - Example: Frontend calls `/login` API to authenticate users.

4. **What is REST API?**
   - REST is an architectural style using HTTP methods.
   - Example:
     - GET `/users`
     - POST `/login`

5. **What does Stateless mean?**
   - Server does not store client session state.
   - Example: JWT token sent with every request.

---

## 🟡 Authentication & Security

6. **What is Authentication?**
   - Process of verifying user identity.
   - Example: Username + password → login success.

7. **What is Authorization?**
   - Process of checking user permissions.
   - Example: Admin can delete users, normal user cannot.

8. **What is JWT?**
   - JSON Web Token used for stateless authentication.
   - Example: Token issued at login, verified on each request.

9. **Why JWT is faster than session-based auth?**
   - No DB lookup needed; token verification is cryptographic.

10. **What is OAuth?**
    - Authorization framework for third-party access.
    - Example: Login with Google / GitHub.

---

## 🟡 Performance & Scalability

11. **What is Caching?**
    - Storing frequently accessed data in memory.
    - Example: Redis cache for dashboard stats.

12. **What is Cache Hit and Cache Miss?**
    - Cache Hit: Data found in cache.
    - Cache Miss: Data fetched from DB and stored in cache.

13. **What is Load Balancer?**
    - Distributes traffic across multiple servers.
    - Example: Nginx, AWS ALB.

14. **What is Horizontal Scaling?**
    - Adding more servers to handle traffic.
    - Example: 1 server → 5 servers.

15. **What is Vertical Scaling?**
    - Increasing CPU/RAM of a server.

---

## 🟡 Databases & Storage

16. **What is Database Indexing?**
    - Index improves search performance.
    - Example: Index on `email` column for fast lookup.

17. **Why indexes slow down writes?**
    - Index needs to be updated on INSERT/UPDATE.

18. **What is Connection Pooling?**
    - Reusing DB connections.
    - Example: 10 connections shared across requests.

19. **What is ACID?**
    - Atomicity, Consistency, Isolation, Durability.
    - Example: Bank transaction must be fully completed or rolled back.

20. **What is Database Transaction?**
    - Group of operations executed as one unit.

---

## 🔴 Advanced Backend Concepts

21. **What is Asynchronous Processing?**
    - Non-blocking execution of tasks.
    - Example: Sending email after API response.

22. **What is Background Job?**
    - Long-running tasks executed outside request lifecycle.
    - Example: OCR processing, report generation.

23. **What is Message Queue?**
    - Decouples producers and consumers.
    - Example: API pushes job → worker processes it.

24. **What is Rate Limiting?**
    - Restricts number of requests per user.
    - Example: 100 requests/minute per IP.

25. **What is Circuit Breaker Pattern?**
    - Prevents repeated calls to failing services.
    - Example: Stop calling OCR API if it is down.

---

## 🔴 System Design Concepts

26. **What is System Design?**
    - Designing scalable, reliable, and maintainable systems.
    - Example: Designing URL shortener, chat system.

27. **What is High Availability?**
    - System remains operational even if one server fails.
    - Example: Multiple backend replicas.

28. **What is Fault Tolerance?**
    - System continues working despite failures.
    - Example: Retry mechanisms, fallbacks.

29. **What is CAP Theorem?**
    - Consistency, Availability, Partition tolerance.
    - Distributed systems choose any two.

30. **What is Microservices Architecture?**
    - Application split into small independent services.
    - Example: Auth service, Payment service.

---

## 🔴 APIs & Communication

31. **What is API Gateway?**
    - Entry point for all client requests.
    - Handles auth, rate limiting, routing.

32. **What is WebSocket?**
    - Persistent connection for real-time communication.
    - Example: Live chat, real-time alerts.

33. **Difference between REST and WebSocket?**
    - REST: Request–response.
    - WebSocket: Continuous bi-directional connection.

34. **What is gRPC?**
    - High-performance RPC framework using Protobuf.
    - Faster than REST for internal services.

35. **What is Idempotency?**
    - Multiple identical requests give same result.
    - Example: Payment API with idempotency key.

---

## 🔴 Monitoring & Reliability

36. **What is Logging?**
    - Recording system events.
    - Example: Error logs, access logs.

37. **What is Monitoring?**
    - Tracking system health.
    - Example: CPU, memory, latency metrics.

38. **What is Observability?**
    - Logs + metrics + traces to understand system behavior.

39. **What is a Health Check Endpoint?**
    - API to verify service health.
    - Example: `/health → 200 OK`.

40. **What is SLA, SLO, and SLI?**
    - SLA: Agreement
    - SLO: Objective
    - SLI: Measurement

---

## 🔴 Security & Best Practices

41. **What is CORS?**
    - Controls cross-origin requests.
    - Example: Frontend domain allowed to call backend.

42. **What is CSRF?**
    - Attack using authenticated user’s session.
    - Prevention: CSRF tokens.

43. **What is SQL Injection?**
    - Malicious SQL queries via input.
    - Prevention: Prepared statements.

44. **What is HTTPS?**
    - Encrypted communication using TLS.

45. **What is Secrets Management?**
    - Secure storage of API keys and passwords.
    - Example: Environment variables, Vault.

---

## 🔴 Real-World Design Scenarios

46. **How do you design a login system?**
    - Password hashing → JWT → role-based access.

47. **How do you design a file upload system?**
    - Upload → validate → store (S3) → async processing.

48. **How do you design a notification system?**
    - Event → Queue → Worker → Email/SMS.

49. **How do you handle third-party API failure?**
    - Timeout + retry + fallback response.

50. **How do you make backend scalable?**
    - Stateless APIs, caching, load balancer, horizontal scaling.

---


---
> 📌 **Note**  
> Follow me on [LinkedIn](https://www.linkedin.com/in/shubham-gupta-92244a200/) and [GitHub](https://github.com/Shubhamgupta171) for preparation guides, interview tips, and related resources.  
>  
> Let's connect and grow together 🚀
---
