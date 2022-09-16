# Project: Blog

> Chuc nang

1. Article manager

   1.1. Article model

   - id
   - authorid
   - title
   - content
   - categoryid
   - createdAt
   - updatedAt
   - tags
   - viewcount

     1.2. category model

   - id
   - name

     1.3. them bai viet

   - input: title, content, tags, categoryid, authorid

     1.4. sua bai viet

   - input: title, content, tags, categoryid

     1.5. xoa bai viet

     1.6. lay noi dung bai viet dua tren id

   - input: id

   - ouput: article

     1.7. lay danh sach bai viet cua category

   - input: categoryid

   - output: array of article + paging

     1.8. lay danh sach bai viet dua tren tags

   - input: tag

   - output: array of article + paging

     1.9. lay danh sach bai viet theo userid

   - input: userid

   - output: array of article + paging

2. Trang profile

   2.1. danh sach bai viet cua user - ref: 1.9

   2.2. hien thi danh sach cac bai viet da duoc bookmark

   - input:

   - output: array of article bookmarked + paging

3. User manager

   3.1. user model

   - username - nvarchar
   - pasword - varchar
   - userid - int
   - email - varchar
   - displayname - nvarchar
   - status - int (-1: banned, 0: deactive, 1: active)

     3.2. dang ky tai khoan

   - input: username, password, email, status = 1

     3.3. reset mat khau

   - input: username/email

   - output: gui email reset mat khau

     3.4. dang nhap

   - input: username, passowrd

   - output: Json web token/refresh token

     3.5. dang xuat

     3.6. show danh sach user

4. comment

   4.1. comment model

   - id
   - authorid
   - createdAt
   - content
   - updatedAt

     4.2. them comment vao article

   - input: content

     4.3. sua comment

   - input: content

     4.4. xoa comment

5. reaction

   5.1. like bai viet

   - input: authorid, articleId

6. share

   - build link share

7. search

   - search: tags, category, username
