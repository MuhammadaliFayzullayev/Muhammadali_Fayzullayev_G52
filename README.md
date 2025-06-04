# 1. Table

```sql
CREATE TABLE roles
(
    id       SERIAL PRIMARY KEY,
    roleName VARCHAR UNIQUE NOT NULL CHECK (roleName IN ('STUDENT', 'MENTOR'))
);
```

***

# 2. Table

```sql
CREATE TABLE users
(
    id       SERIAL PRIMARY KEY,
    fullName VARCHAR CHECK (char_length(fullName) >= 5),
    phone    VARCHAR(9) UNIQUE CHECK (char_length(phone) = 9),
    role_id  INT,
    FOREIGN KEY (role_id) REFERENCES roles (id) ON DELETE SET NULL
);
-- INSERTIONS

----------users insert-------------------------------
insert into users (fullName, phone, role_id)
values ('Leicester Gadie', null, null);
insert into users (fullName, phone, role_id)
values ('Wandie Adess', null, null);
insert into users (fullName, phone, role_id) values ('Tansy Andrivot', null, null);
insert into users (fullName, phone, role_id) values ('Elfrieda Skpsey', null, null);
insert into users (fullName, phone, role_id) values ('Montague Schuchmacher', null, null);
insert into users (fullName, phone, role_id) values ('Brewer Minshull', null, null);
insert into users (fullName, phone, role_id) values ('Bethanne Caudray', null, null);
insert into users (fullName, phone, role_id) values ('Joanie Frediani', null, null);
insert into users (fullName, phone, role_id) values ('Arnie Blesdill', null, null);
insert into users (fullName, phone, role_id) values ('Keir Synke', null, null);
insert into users (fullName, phone, role_id) values ('Costa Neligan', null, null);
insert into users (fullName, phone, role_id) values ('Saba Cridlan', null, null);
insert into users (fullName, phone, role_id) values ('Margaretha Andrzejowski', null, null);
insert into users (fullName, phone, role_id) values ('Kipp Crapper', null, null);
insert into users (fullName, phone, role_id) values ('Bella Pennazzi', null, null);
insert into users (fullName, phone, role_id) values ('Dulcy Gonthier', null, null);
insert into users (fullName, phone, role_id) values ('Agace Highman', null, null);
insert into users (fullName, phone, role_id) values ('Fredia Westphal', null, null);
insert into users (fullName, phone, role_id) values ('Fayette Torn', null, null);
insert into users (fullName, phone, role_id) values ('Whitney Esley', null, null);
insert into users (fullName, phone, role_id) values ('Edi Leehane', null, null);
insert into users (fullName, phone, role_id) values ('Jake Aizik', null, null);
insert into users (fullName, phone, role_id) values ('Romona Casiroli', null, null);
insert into users (fullName, phone, role_id) values ('Tyler Pruckner', null, null);
insert into users (fullName, phone, role_id) values ('Christan Mollen', null, null);
insert into users (fullName, phone, role_id) values ('Dani Quainton', null, null);
insert into users (fullName, phone, role_id) values ('Roi Notti', null, null);
insert into users (fullName, phone, role_id) values ('Ariadne Rackley', null, null);
insert into users (fullName, phone, role_id) values ('Vilma Aubin', null, null);
insert into users (fullName, phone, role_id) values ('Grant Gronowe', null, null);
insert into users (fullName, phone, role_id) values ('Ottilie Airth', null, null);
insert into users (fullName, phone, role_id) values ('Tami Hallawell', null, null);
insert into users (fullName, phone, role_id) values ('Row Stocking', null, null);
insert into users (fullName, phone, role_id) values ('Evita Fitkin', null, null);
insert into users (fullName, phone, role_id) values ('Matelda Hevey', null, null);
insert into users (fullName, phone, role_id) values ('Guglielma Giffard', null, null);
insert into users (fullName, phone, role_id) values ('Chrotoem Millmoe', null, null);
insert into users (fullName, phone, role_id) values ('Isaak Postins', null, null);
insert into users (fullName, phone, role_id) values ('Saul Edison', null, null);
insert into users (fullName, phone, role_id) values ('Percy Risebrow', null, null);
insert into users (fullName, phone, role_id) values ('Tomasine Cuffe', null, null);
insert into users (fullName, phone, role_id) values ('Freida Du Pre', null, null);
insert into users (fullName, phone, role_id) values ('Quinn Gradwell', null, null);
insert into users (fullName, phone, role_id) values ('Lavinie Bartolomieu', null, null);
insert into users (fullName, phone, role_id) values ('Debee Tembridge', null, null);
insert into users (fullName, phone, role_id) values ('Price Latey', null, null);
insert into users (fullName, phone, role_id) values ('Gussy Lehon', null, null);
insert into users (fullName, phone, role_id) values ('Edouard Nussen', null, null);
insert into users (fullName, phone, role_id) values ('Merralee Bowmaker', null, null);
insert into users (fullName, phone, role_id) values ('Nollie McSwan', null, null);
insert into users (fullName, phone, role_id) values ('Manolo MacKniely', null, null);
insert into users (fullName, phone, role_id) values ('Alec Davio', null, null);
insert into users (fullName, phone, role_id) values ('Franny Castello', null, null);
insert into users (fullName, phone, role_id) values ('Marcile Passo', null, null);
insert into users (fullName, phone, role_id) values ('Helen-elizabeth Heyward', null, null);
insert into users (fullName, phone, role_id) values ('Tanya Denys', null, null);
insert into users (fullName, phone, role_id) values ('Ronnie Celler', null, null);
insert into users (fullName, phone, role_id) values ('Maggee Crim', null, null);
insert into users (fullName, phone, role_id) values ('Adelheid Levick', null, null);
insert into users (fullName, phone, role_id) values ('Ario Bilfoot', null, null);
insert into users (fullName, phone, role_id) values ('Mersey Kilmister', null, null);
insert into users (fullName, phone, role_id) values ('Thor King', null, null);
insert into users (fullName, phone, role_id) values ('Yasmin Killingbeck', null, null);
insert into users (fullName, phone, role_id) values ('Heath Archdeacon', null, null);
insert into users (fullName, phone, role_id) values ('Kamila McEneny', null, null);
insert into users (fullName, phone, role_id) values ('Zacharie Bermingham', null, null);
insert into users (fullName, phone, role_id) values ('Allard Hulett', null, null);
insert into users (fullName, phone, role_id) values ('Verine Griffithe', null, null);
insert into users (fullName, phone, role_id) values ('Roseanne Calvey', null, null);
insert into users (fullName, phone, role_id) values ('Marilyn Alps', null, null);
insert into users (fullName, phone, role_id) values ('Arvin Chaloner', null, null);
insert into users (fullName, phone, role_id) values ('Byrann Mustarde', null, null);
insert into users (fullName, phone, role_id) values ('Perry Matej', null, null);
insert into users (fullName, phone, role_id) values ('Anallise Sokale', null, null);
insert into users (fullName, phone, role_id) values ('Janna Shilladay', null, null);
insert into users (fullName, phone, role_id) values ('Annabel Edwicker', null, null);
insert into users (fullName, phone, role_id) values ('Berton Gambles', null, null);
insert into users (fullName, phone, role_id) values ('Sonya Ortas', null, null);
insert into users (fullName, phone, role_id) values ('Bebe Lethley', null, null);
insert into users (fullName, phone, role_id) values ('Silvain Stell', null, null);
insert into users (fullName, phone, role_id) values ('Hamilton Ransfield', null, null);
insert into users (fullName, phone, role_id) values ('Tammi Chater', null, null);
insert into users (fullName, phone, role_id) values ('Hewet Foystone', null, null);
insert into users (fullName, phone, role_id) values ('Vick Huntar', null, null);
insert into users (fullName, phone, role_id) values ('Doreen Smithies', null, null);
insert into users (fullName, phone, role_id) values ('Abbie Moffett', null, null);
insert into users (fullName, phone, role_id) values ('Enriqueta Oleszkiewicz', null, null);
insert into users (fullName, phone, role_id) values ('Joelly Martel', null, null);
insert into users (fullName, phone, role_id) values ('Tani Dunstan', null, null);
insert into users (fullName, phone, role_id) values ('Gannie Sybbe', null, null);
insert into users (fullName, phone, role_id) values ('Sydel Castelluzzi', null, null);
insert into users (fullName, phone, role_id) values ('Beryl Willows', null, null);
insert into users (fullName, phone, role_id) values ('Cassie Foster', null, null);
insert into users (fullName, phone, role_id) values ('Roxy Coultish', null, null);
insert into users (fullName, phone, role_id) values ('Clare Imlach', null, null);
insert into users (fullName, phone, role_id) values ('Drusilla Allix', null, null);
insert into users (fullName, phone, role_id) values ('Christin Hammett', null, null);
insert into users (fullName, phone, role_id) values ('Mil Paulsson', null, null);
insert into users (fullName, phone, role_id) values ('Bobette Dowty', null, null);
insert into users (fullName, phone, role_id) values ('Marieann Slot', null, null);
```

***

# 3. Table

```sql
CREATE TABLE groups
(
    id        SERIAL PRIMARY KEY,
    groupName VARCHAR CHECK (char_length(groupName) >= 3),
    mentor_id INT,
    createdAt DATE NOT NULL DEFAULT CURRENT_DATE,
    FOREIGN KEY (mentor_id) REFERENCES users (id) ON DELETE SET NULL
);
-------------groups insert----------------------
INSERT INTO groups (groupname, mentor_id) VALUES
                                              ('Group1', 1),
                                              ('Group2', 2),
                                              ('Group3', 3),
                                              ('Group5', 4),
                                              ('Group6', 5),
                                              ('Group7', 6),
                                              ('Group8', NULL),
                                              ('Group9', NULL);
```
***

# 4. Table

```sql
CREATE TABLE students
(
    id        SERIAL PRIMARY KEY,
    user_id   INT UNIQUE,
    group_id  INT,
    createdAt DATE    NOT NULL DEFAULT CURRENT_DATE,
    active    BOOLEAN NOT NULL DEFAULT FALSE,
    FOREIGN KEY (user_id) REFERENCES users (id) ON DELETE CASCADE,
    FOREIGN KEY (group_id) REFERENCES groups (id) ON DELETE CASCADE
);
-- INSERT lar
---------------------students insert----------------------
INSERT INTO students (user_id, group_id, active) VALUES
                                                     (7, 1, true),
                                                     (8, 1, false),
                                                     (9, 2, true),
                                                     (10, 2, false),
                                                     (11, 3, true),
                                                     (12, 3, false),
                                                     (13, 4, true),
                                                     (14, 4, false),
                                                     (15, 5, true),
                                                     (16, 5, false),
                                                     (17, 6, true),
                                                     (18, 6, false),
                                                     (19, 1, true),
                                                     (20, 1, false),
                                                     (21, 2, true),
                                                     (22, 2, false),
                                                     (23, 3, true),
                                                     (24, 3, false),
                                                     (25, 4, true),
                                                     (26, 4, false),
                                                     (27, 5, true),
                                                     (28, 5, false),
                                                     (29, 6, true),
                                                     (30, 6, false),
                                                     (31, 1, true),
                                                     (32, 1, false),
                                                     (33, 2, true),
                                                     (34, 2, false),
                                                     (35, 3, true),
                                                     (36, 3, false),
                                                     (37, 4, true),
                                                     (38, 4, false),
                                                     (39, 5, true),
                                                     (40, 5, false),
                                                     (41, 6, true),
                                                     (42, 6, false),
                                                     (43, 1, true),
                                                     (44, 1, false),
                                                     (45, 2, true),
                                                     (46, 2, false),
                                                     (47, 3, true),
                                                     (48, 3, false),
                                                     (49, 4, true),
                                                     (50, 4, false),
                                                     (51, 5, true),
                                                     (52, 5, false),
                                                     (53, 6, true),
                                                     (54, 6, false),
                                                     (55, 1, true),
                                                     (56, 1, false),
                                                     (57, 2, true),
                                                     (58, 2, false),
                                                     (59, 3, true),
                                                     (60, 3, false),
                                                     (61, 4, true),
                                                     (62, 4, false),
                                                     (63, 5, true),
                                                     (64, 5, false),
                                                     (65, 6, true),
                                                     (66, 6, false),
                                                     (67, 1, true),
                                                     (68, 1, false),
                                                     (69, 2, true),
                                                     (70, 2, false),
                                                     (71, 3, true),
                                                     (72, 3, false),
                                                     (73, 4, true),
                                                     (74, 4, false),
                                                     (75, 5, true),
                                                     (76, 5, false),
                                                     (77, 6, true),
                                                     (78, 6, false),
                                                     (79, 1, true),
                                                     (80, 1, false),
                                                     (81, 2, true),
                                                     (82, 2, false),
                                                     (83, 3, true),
                                                     (84, 3, false),
                                                     (85, 4, true),
                                                     (86, 4, false),
                                                     (87, 5, true),
                                                     (88, 5, false),
                                                     (89, 6, true),
                                                     (90, 6, false);


INSERT INTO students (user_id, group_id, active) VALUES
                                                     (91, NULL, false),
                                                     (92, NULL, false),
                                                     (93, NULL, false),
                                                     (94, NULL, false),
                                                     (95, NULL, false),
                                                     (96, NULL, false),
                                                     (97, NULL, false),
                                                     (98, NULL, false),
                                                     (99, NULL, false),
                                                     (100, NULL, false);
```

# 2. Standard VIEW
```sql
CREATE OR REPLACE VIEW students_view AS
SELECT
    s.id AS student_id,
    u.fullName AS student_fullName,
    s.createdAt AS student_createdAt,
    g.groupName,
    mu.fullName AS mentor_fullName
FROM students s
         JOIN users u ON s.user_id = u.id
         LEFT JOIN groups g ON s.group_id = g.id
         LEFT JOIN users mu ON g.mentor_id = mu.id
ORDER BY s.createdAt DESC
LIMIT 10;
```
***
# 3. Materialized VIEW
```sql
CREATE MATERIALIZED VIEW M_view AS
SELECT
    g.id AS group_id,
    g.groupName,
    g.createdAt AS group_createdAt,
    COUNT(s.id) AS studentCount
FROM groups g
         LEFT JOIN students s ON g.id = s.group_id
GROUP BY g.id
ORDER BY studentCount DESC
LIMIT 3;
-- Materialized VIEW refresh qilish orqali yangi malumotlarni saqlaydi
REFRESH MATERIALIZED VIEW top_3_groups_view;
```
***
# 4. Create function
```sql
----------------------FUNCTION---------------------------
CREATE OR REPLACE FUNCTION groupOfMentor(p_mentor_id INT)
    RETURNS TABLE (
                      mentor_id INT,
                      mentor_fullName VARCHAR,
                      groupName VARCHAR,
                      group_createdAt DATE,
                      studentCount INT
                  ) AS $$
BEGIN
    RETURN QUERY
        SELECT
            g.mentor_id,
            mu.fullName,
            g.groupName,
            g.createdAt,
            COUNT(s.id) AS studentCount
        FROM groups g
                 LEFT JOIN users mu ON g.mentor_id = mu.id
                 LEFT JOIN students s ON g.id = s.group_id
        WHERE g.mentor_id = p_mentor_id
        GROUP BY g.id, mu.fullName;
END;
$$ LANGUAGE plpgsql;
```
***
# 5. Create  PROCEDURE
```sql
CREATE OR REPLACE PROCEDURE studentActivator(p_group_id INT)
    LANGUAGE plpgsql
AS $$
BEGIN
    UPDATE students
    SET active = TRUE
    WHERE group_id = p_group_id AND active = FALSE;
END;
$$;

CALL studentActivator(2);
```
***
# 6. Trigger
```sql
-- Changelog table yaratiladi
CREATE TABLE change_logs (
                             id SERIAL PRIMARY KEY,
                             table_name VARCHAR,
                             operation_type VARCHAR, -- 'UPDATE'
                             changed_at TIMESTAMP DEFAULT now(),
                             old_data JSONB,
                             new_data JSONB
);

-- Trigger logic yaratiladi
CREATE OR REPLACE FUNCTION log_update_changes()
    RETURNS TRIGGER AS $$
BEGIN
    INSERT INTO change_logs(table_name, operation_type, old_data, new_data)
    VALUES (
               TG_TABLE_NAME,
               TG_OP,
               to_jsonb(OLD),
               to_jsonb(NEW)
           );
    RETURN NEW;
END;
$$ LANGUAGE plpgsql;

-- TRIGGER yaratiladi
CREATE TRIGGER trg_log_students_update
    AFTER UPDATE ON students
    FOR EACH ROW
EXECUTE FUNCTION log_update_changes();


CREATE TRIGGER trg_log_groups_update
    AFTER UPDATE ON groups
    FOR EACH ROW
EXECUTE FUNCTION log_update_changes();
```
***
MuhammadaliFayzullayev/Muhammadali_Fayzullayev_G52

# Savollarga javoblar:
# 1 - savol
Malumotlarning tartibli to`plami
***
# 2 - savol
RDBMS — bu ma’lumotlarni jadval (table) ko‘rinishida saqlaydigan va ular o‘rtasidagi aloqalarni (relationship) boshqaradigan DBMS turidir
***
# 3 - savol
`DBMS` - o'z nomi bilan, to'liq ma'lumotlar oqimini boshqarishda ishlatilinadigan boshqaruv tizimi hisoblanib, u orqali malumot 
saqlanishi, olinishi va bu jarayonlarning qanchalik tez yoki sekin bolishini o'z zimmasiga oluvchi dasturiy taminot.
`RDBMS` - yani Relational DBMS xuddi DBMS ga o'xshash xususiyatlarga ega, lekin ma'lumotlar o'rtasida bog'liqliklar yaratish
imkonini beruvchi ma'lumotlar bazasi boshqarish tizimi hisoblanadi. Unda DBMS dan farqli o'laroq, ikki jadvalda malum ustunlar
o'rtasida FOREIGN KEY lar va maxsus cheklovlar orqali bog'liqlik yaratish mumkin.
***
# 4  - savol
SQL — bu Structured Query Language degan so‘zlarning qisqartmasi bo‘lib, ma’lumotlar bazasini boshqarish va ulardan ma’lumot olish uchun ishlatiladigan til hisoblanadi.
***

# 5 - savol
PL/pgSQL — bu PostgreSQL ma’lumotlar bazasi uchun yaratilgan protsedura tillaridan biri (Procedural Language).
PostgreSQLda server tomonida bajariladigan dasturlash tili.
SQL so‘rovlarini protsedural kodga (funksiyalar, triggerlar) aylantirish imkonini beradi.
Dasturlash tillariga xos shartlar, sikllar, o‘zgaruvchilar, istisno tutish kabi imkoniyatlarni qo‘llab-quvvatlaydi.
Ma’lumotlar bazasidagi murakkab ishlarni soddalashtirish uchun ishlatiladi.
*** 
# 6 - savol
Primary Key va Foreign Key — ma’lumotlar bazasidagi jadvallar orasidagi bog‘lanishni ta’minlovchi va ma’lumotlarni yaxlitligini (integrity) saqlovchi asosiy kalitlar.
Primary Key (Asosiy kalit) nima?
Har bir jadvalda yagona va noyob qiymatga ega bo‘lgan ustun yoki ustunlar to‘plami.
Jadvaldagi har bir qatorni unikal tarzda identifikatsiyalash uchun ishlatiladi.
Primary key qiymatlari NULL bo‘lishi mumkin emas.
Odatda bitta jadvalda faqat bitta primary key bo‘ladi.
***
# 7 - savol
`ASSERT` statement — bu dasturda kutilgan shart bajarilganini tekshirish uchun ishlatiladi. Agar shart bajarilmasa, xatolik
yuz beradi. Bu asosan test qilish jarayonlarida ishlatiladi. Bu orqali database da noto'g'ri amaliyot bo'lmasligini
tekshirish mumkin. Asosiy maqsad - xatolik yuzaga kelishi mumkin bo'lgan holatlarda oldindan tekshirib kamchiliklarni oldini olish!

# 8 - savol
Trigger — bu ma’lumotlar bazasida avtomatik ishga tushadigan maxsus kod blok.
***

# 9 - savol
Transaction — bu ma’lumotlar bazasida bajariladigan bir nechta SQL buyruqlari bitta yagona ish birligi sifatida.
Ya’ni, u yoki hammasi bajariladi, yoki hech biri bajarilmaydi.
Masalan, bankda pul o‘tkazishda: hisobdan pul chiqarish va boshqa hisobga qo‘shish — bu ikki amal tranzaksiya bo‘lib, ular birga bajarilishi kerak.
***
# 10
Indexing (Indekslashtirish) — bu ma’lumotlar bazasida ma’lumotlarni tez va samarali qidirish uchun maxsus tuzilgan ma’lumotlar tuzilmasi.
Vazifalari:
Qidiruvni tezlashtiradi: Indekslar yordamida ma’lumotlarni jadval bo‘ylab to‘liq tekshirmasdan, tez topish mumkin.
So‘rovlarni optimallashtiradi: Murakkab SQL so‘rovlari tezroq bajariladi.
Ma’lumotni tartiblaydi: Indekslar ma’lumotlarni ma’lum tartibda saqlashga yordam beradi (masalan, PRIMARY KEY uchun).
***
