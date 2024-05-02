<h1 align="center">Mobile Phone Recycle Web App use Service Based Architecture</h1>
<div align="center">
    <img src="https://techstack-generator.vercel.app/java-icon.svg" alt="icon" width="50" height="50" />
</div>

## 🚩 Mục lục
- [Yêu cầu của bài tập](#yêu-cầu-của-bài-tập) 
- [Diagram](#diagram)
- [Được xây dựng bằng](#được-xây-dựng-bằng)
- [Các dependency sử dụng](#các-dependency-sử-dụng)
- [Demo Chương trình](#demo-chương-trình)

## Yêu cầu của bài tập

- [Đặc tả yêu cầu]
  
  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/ce9b93b5-7691-4def-9dd7-5863312b872d)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/87d4d0ee-e43c-4a2b-8476-75b499dccc39)

## Diagram

  ### Customer Services Diagram
  
  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/0b298e33-f2e0-4fb3-9c5d-85008bc3f8d7)

  ### RecyclingAccountingAssessment Diagram

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/d90c9265-f5e6-45d6-a2c3-93ad9d2a4895)


## Được xây dựng bằng
  ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?logo=java&logoColor=white&style=for-the-badge)
  ![SpringBoot](https://img.shields.io/badge/Spring%20Boot-6DB33F.svg?style=for-the-badge&logo=Spring-Boot&logoColor=white)
  ![React](https://img.shields.io/badge/react-%2320232a.svg?logo=react&logoColor=%2361DAFB&style=for-the-badge)
  ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?logo=spring&logoColor=white&style=for-the-badge)
  ![MariaDB](https://img.shields.io/badge/MariaDB-003545?logo=mariadb&logoColor=white&style=for-the-badge)
  ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?logo=javascript&logoColor=%23F7DF1E&style=for-the-badge)

## Các Dependency sử dụng
 - mariadb-java-client
    + Maven
    ```xml
        <dependency>
            <groupId>org.mariadb.jdbc</groupId>
            <artifactId>mariadb-java-client</artifactId>
            <scope>runtime</scope>
        </dependency>
    ```
 - spring-boot-starter-data-jpa
    + Maven
    ```xml
         <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>
    ```
 - spring-boot-starter-data-jpa
    + Maven
    ```xml
         <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    ```
 - lombok
    + Maven
    ```xml
         <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
        </dependency>
    ```
 - jbcrypt (hash password)
    + Maven
    ```xml
         <dependency>
            <groupId>org.mindrot</groupId>
            <artifactId>jbcrypt</artifactId>
            <version>0.4</version>
        </dependency>
    ```
 - poi (Read file mobile_prices.csv to get price of mobiles)
    + Maven
    ```xml
         <dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi</artifactId>
            <version>5.2.0</version>
        </dependency>
    ```  
 - poi-ooxml (Read file mobile_prices.csv to get price of mobiles)
    + Maven
    ```xml
          <dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi-ooxml</artifactId>
            <version>5.2.0</version>
        </dependency>
    ```  
 - spring-boot-starter-mail (Send email to customer about price suggested by delivery and real price after the device is delivered, request customer login to account to accept real price or rejected)
    + Maven
    ```xml
          <dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi-ooxml</artifactId>
            <version>5.2.0</version>
        </dependency>
    ```

## Demo Chương trình
 * Khách hàng cần đăng ký tài khoản nếu chưa có để có thể nhận báo giá về điện thoại cần tái chế, các thông tin cần thiết là: email (để gửi thông báo cho người dùng khi giá sau kiểm định thực tế khác với giá báo thông qua form khảo sát trên web), tên ngân hàng và tên tài khoản (nhằm mục đích chuyển tiền khi khác hàng đồng ý giá cuối mà bên công ty đưa ra), ngoài ra cần dùng số điện thoại tránh trường hợp email có vấn đề

   ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/973683d4-3fdb-4e3e-8b5e-832ae284b369)

   ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/664e9ac3-1ddf-49ca-87cb-b50d8dd81ed6)

* Khi login vào như Customer người dùng có thể sử dụng dịch vụ báo giá cho điện thoại cần tái chế

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/84dc110d-96e0-47a7-a926-66d128acae4e)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/15356f68-927d-4a99-8ba4-d2684a723acf)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/17a4c321-cd48-42ee-a726-882eaaaa368e)

* Nếu điện thoại nằm trong danh sách số điện thoại mà bên cung cấp dịch cần thì sẽ gửi mức giá đề xuất đì kèm và yêu cầu khách hàng gửi địa chỉ lấy hàng, giá điện thoai ban đầu của mỗi chiếc điện thoại nằm trong file xlsx dựa theo thông tin khách hàng đã nhập đề trừ bớt đi, người dùng
không có quyền nhập mức giá của điện thoại
  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/113d4160-20d0-413a-b17a-7352204d3de4)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/d0fbe985-bd3f-4f93-aa9b-62714a59db36)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/7aee4883-527e-423b-97f7-b8737310e6e8)

* Người dùng có thể xem điện thoại đã gửi đi thông qua List My Items, trang sẽ hiển thị thông tin DeviceId nhằm mục đích giúp khách hàng theo dõi được tình trạng thiết bị khi vận chuyển và xử lý
  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/256786df-fb2e-4283-b35e-ca7f51cf7ff7)

* Khách hàng có thể theo dõi thiết bị của mình (Thêm field số điện thoại nhằm mục đích tăng tính bảo mật, riêng tư)
  
  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/6419ec34-491a-4db2-98a5-2abb37f9d304)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/b5613b1f-21f1-42d4-81b5-4bf693ab4e96)

* Khi đăng nhập như admin thì có thể sử dụng một số chức năng khác như Filter devices by Status

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/ac04807e-4174-4317-a344-ac48227d51db)

  ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/3eda2fcd-36cc-4b16-85ec-82e2cbe02531)

  - Với nhưng đơn đang là delivering thì có thể cập nhật thành Delivered
    
    ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/4f2ef5af-6009-4b84-a9bd-eb0ac9d9ece5)

  - Với những đơn là delivered thì mình có thể gửi thông tin sau khi điểm tra máy trực tiếp (lưu thông tin vào hệ thống và gửi thông báo qua
    email) - 1 Số field là readonly không được chỉnh sửa
    ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/7e7ddf6e-95bb-4014-9f15-800c4c7bfb15)

    ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/6bdcc3ac-0a37-45cb-8c6a-07d06c6d8c1d)

    ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/11b85514-00f1-42d7-85aa-e743050de404)

    ![image](https://github.com/nguyenhieu1435/MobilePhoneRecycle_ServiceBasedArch/assets/70377398/fb69bad6-bfeb-4caf-a29a-4757a4d291f4)






  

  

  

