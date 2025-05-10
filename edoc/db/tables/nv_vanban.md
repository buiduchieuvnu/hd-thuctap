# Table: 
- Desc: Bảng lưu 

- Create table
```sql
create table sample(
   id serial primary key,
   -- FKs
   -- Cột mặc định (bắt buộc có)
   ghichu varchar(200),
   ngaytao timestamp not null,
   nguoitao varchar(200),
   ngaysua timestamp,
   nguoisua varchar(200),
   trangthai int default 1
);

comment on column taikhoan.id is 'Table: lưu ';

comment on column taikhoan.trangthai is 'Trạng thái:
-1: Đã xóa
0: Khóa
1: Sử dụng
';
```
- FK
```sql
```


