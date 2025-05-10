# hoso
- Desc: Bảng lưu thông tin hồ sơ người dùng

- Create table
```sql
create table ht_hoso(
   id serial primary key,
   hoten varchar(200) not null,
   dienthoai varchar(20) not null,
   email varchar(100) not null,
   ngaysinh timestamp,
   -- Cột mặc định (bắt buộc có)
   ghichu varchar(200),
   ngaytao timestamp not null,
   nguoitao varchar(200),
   ngaysua timestamp,
   nguoisua varchar(200),
   trangthai int default 1
);

comment on column ht_hoso.id is 'Table: lưu thông tin hồ sơ người dùng';

comment on column ht_hoso.trangthai is 'Trạng thái:
-1: Đã xóa
0: Khóa
1: Sử dụng
2: Tạm đình chỉ
3: Đã nghỉ hưu
';
```

