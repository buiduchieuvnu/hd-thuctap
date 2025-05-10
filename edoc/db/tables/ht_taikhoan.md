# Tài khoản
- Desc: Bảng lưu thông tin tài khoản

- Create table
```sql
create table ht_taikhoan(
   id serial primary key,
   taikhoan varchar(200) not null,
   matkhau varchar(500) not null,
   -- FKs
   hoso_id int not null,
   -- Cột mặc định (bắt buộc có)
   ghichu varchar(200),
   ngaytao timestamp not null,
   nguoitao varchar(200),
   ngaysua timestamp,
   nguoisua varchar(200),
   trangthai int default 1
);

comment on column ht_taikhoan.id is 'Table: lưu thông tin tài khoản';

comment on column ht_taikhoan.trangthai is 'Trạng thái:
-1: Đã xóa
0: Khóa
1: Sử dụng
';
```
- FK
```sql
comment on column ht_taikhoan.hoso_id is 'FK: Hồ sơ';
alter table ht_taikhoan add constraint fk_hsid foreign key (hoso_id) references hoso(id);
```


