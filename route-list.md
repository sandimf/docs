---
description: >-
  Route melihat menampilkan route yang tersedia dengan metode request yang
  berbeda beda.
---

# Route List

```php
  GET|HEAD        / ............................................................................................................................................................ home
  GET|HEAD        api/user .......................................................................................................................................................... 
  GET|HEAD        api/v1/screenings .......................................................................................... screenings.index › Api\V1\ScreeningApiController@index
  POST            api/v1/screenings .......................................................................................... screenings.store › Api\V1\ScreeningApiController@store
  GET|HEAD        api/v1/screenings/{screening} ................................................................................ screenings.show › Api\V1\ScreeningApiController@show
  PUT|PATCH       api/v1/screenings/{screening} ............................................................................ screenings.update › Api\V1\ScreeningApiController@update
  DELETE          api/v1/screenings/{screening} .......................................................................... screenings.destroy › Api\V1\ScreeningApiController@destroy
  GET|HEAD        auth/{provider}/callback ......................................................................................................... Auth\ProviderController@callback
  GET|HEAD        auth/{provider}/redirect ......................................................................................................... Auth\ProviderController@redirect
  GET|HEAD        blog ...................................................................................................................... blogs.index › Blog\BlogController@index
  GET|POST|HEAD   broadcasting/auth ...................................................................................... Illuminate\Broadcasting › BroadcastController@authenticate
  GET|HEAD        community ......................................................................................................... community › Community\CommunityController@index
  POST            community ................................................................................................... community.store › Community\CommunityController@store
  GET|HEAD        community/post ................................................................................................ community.post › Community\CommunityController@post
  GET|HEAD        community/profile/{uuid} ........................................................................... community.profile › Community\ProfileCommunityController@Index
  GET|HEAD        community/reply ............................................................................................. community.reply › Community\CommunityController@reply
  POST            community/usernme ............................................................................... community.setUsername › Community\CommunityController@setUsername
  GET|HEAD        confirm-password ....................................................................................... password.confirm › Auth\ConfirmablePasswordController@show
  POST            confirm-password ......................................................................................................... Auth\ConfirmablePasswordController@store
  GET|HEAD        contact .................................................................................................................... contact › Page\ContactController@Index
  GET|HEAD        dashboard ................................................................................................................ dashboard › User\PatientController@index
  GET|HEAD        dashboard/admin ...................................................................................................... admin.dashboard › User\AdminController@index
  GET|HEAD        dashboard/admin/blog/new ................................................................................................... blog.post › Blog\BlogController@create
  POST            dashboard/admin/blog/store ................................................................................................. blog.store › Blog\BlogController@store
  GET|HEAD        dashboard/admin/community/list ............................................................................. admin.community › Community\CommunityController@Approv
  DELETE          dashboard/admin/community/{id} .......................................................................... community.destroy › Community\CommunityController@destroy
  POST            dashboard/admin/community/{id}/approve .................................................................. community.approve › Community\CommunityController@approve
  GET|HEAD        dashboard/admin/product/category ............................................................................ category.create › Ecommerce\CategoryController@create
  POST            dashboard/admin/product/category/store ........................................................................ category.store › Ecommerce\CategoryController@store
  GET|HEAD        dashboard/admin/product/list ...................................................................................... product.list › Clinic\EcommerceController@index
  GET|HEAD        dashboard/admin/product/new ................................................................................... product.create › Ecommerce\ProductController@create
  POST            dashboard/admin/product/store .................................................................................. products.store › Ecommerce\ProductController@store
  GET|HEAD        dashboard/admin/profile .............................................................................................. admin.profile › User\AdminController@profile
  GET|HEAD        dashboard/admin/scan ....................................................................................................... admin.scan › User\AdminController@scan
  POST            dashboard/admin/scan/process ..................................................................................... admin.scan.process › User\AdminController@scanQr
  GET|HEAD        dashboard/admin/users .................................................................................................... users.admin › User\AdminController@Users
  GET|HEAD        dashboard/admin/users/new ............................................................................................... users.new › User\AdminController@addUsers
  POST            dashboard/admin/users/store .......................................................................................... users.store › User\AdminController@storeUser
  GET|HEAD        dashboard/appointment ............................................................................................ appointment › Clinic\AppointmentController@index
  POST            dashboard/appointment ..................................................................................... appointment.create › Clinic\AppointmentController@store
  GET|HEAD        dashboard/appointment/list ........................................................... patient.appointments.list › Clinic\AppointmentController@patientAppointments
  GET|HEAD        dashboard/appointment/medical-record/{appointment} ................................. patients.medical-record › Clinic\AppointmentController@showMedicalRecordDetail
  GET|HEAD        dashboard/cashier ................................................................................................ cashier.dashboard › User\CashierController@index
  GET|HEAD        dashboard/cashier/daily-report ............................................................... cashier.dailyReport › UserReport\CashierReportController@dailyReport
  GET|HEAD        dashboard/cashier/payment-history ................................................................................ cashier.history › User\CashierController@history
  POST            dashboard/cashier/payment/offline/{id} ..................................................... cashier.payment.offline › User\CashierController@confirmPaymentOffline
  POST            dashboard/cashier/payment/online/{id} .......................................................... cashier.confirmPayment › Screening\OnlineController@confirmPayment
  GET|HEAD        dashboard/cashier/profile ........................................................................................ cashier.profile › User\CashierController@profile
  GET|HEAD        dashboard/cashier/report ................................................................................ cashier.report › UserReport\CashierReportController@index
  GET|HEAD        dashboard/cashier/screening/offline ........................................................... cashier.screening.offline › User\CashierController@ScreeningOffline
  GET|HEAD        dashboard/cashier/screening/online ................................................... cashier.screening.online › Screening\OnlineController@ScreeningOnlinePayment
  GET|HEAD        dashboard/cashier/screening/payment/{id} ......................................................................... payment.cashier › User\CashierController@Payment
  GET|HEAD        dashboard/cordi ...................................................................................................... cordi.dashboard › User\CordiController@index
  GET|HEAD        dashboard/cordi/emergency/{id}/{status} .......................................................... emergency.status.store › Clinic\EmergencyController@updateStatus
  GET|HEAD        dashboard/cordi/history ........................................................................... emergency.history.cordi › User\CordiController@emergencyHistory
  GET|HEAD        dashboard/doctor ................................................................................................... doctor.dashboard › User\DoctorController@index
  GET|HEAD        dashboard/doctor/appointment ............................................................................... doctor.appointment › User\DoctorController@Appointment
  POST            dashboard/doctor/appointments/{appointment}/medical-record .................. doctor.appointments.medical-record › Clinic\AppointmentController@updateMedicalRecord
  PUT             dashboard/doctor/appointments/{id}/complete .................................................. doctor.appointments.complete › Clinic\AppointmentController@complete
  PUT             dashboard/doctor/appointments/{id}/confirm ..................................................... doctor.appointments.confirm › Clinic\AppointmentController@confirm
  GET|HEAD        dashboard/doctor/medical-record/detail/{id} ............................. doctor.medical_record.detail › Clinic\AppointmentController@showMedicalRecordDetailDoctor
  GET|HEAD        dashboard/doctor/medical-record/{appointment} .............................................. doctor.medical_record › Clinic\AppointmentController@showMedicalRecord
  GET|HEAD        dashboard/doctor/physical/{id} ........................................................................ doctor.physical › User\DoctorController@PhysicalExamination
  GET|HEAD        dashboard/doctor/profile ........................................................................................... doctor.profile › User\DoctorController@profile
  GET|HEAD        dashboard/doctor/screening ....................................................................... doctor.OfflineScreening › User\DoctorController@OfflineScreening
  POST            dashboard/doctor/screening/health-check/{id} ........................................................ health.check.doctor › User\DoctorController@updateHealthCheck
  GET|HEAD        dashboard/doctor/screening/{id} ................................................................... doctor.screeningDetail › User\DoctorController@QuestionerDetail
  GET|HEAD        dashboard/emergency ................................................................................................. emergency › Clinic\EmergencyController@create
  POST            dashboard/emergency ............................................................................................ emergency_store › Clinic\EmergencyController@store
  GET|HEAD        dashboard/emergency/history ...................................................................................... emergency_show › Clinic\EmergencyController@show
  GET|HEAD        dashboard/manager ................................................................................................ manager.dashboard › User\ManagerController@index
  GET|HEAD        dashboard/manager/profile ........................................................................................ manager.profile › User\ManagerController@profile
  GET|HEAD        dashboard/manager/report .................................................................................... report.manager › User\ManagerController@reportManager
  GET|HEAD        dashboard/manager/report/pdf .............................................................................. manager.report.pdf › User\ManagerController@generatePDF
  GET|HEAD        dashboard/manager/screening ........................................................................... screening.manager › User\ManagerController@ScreeningOffline
  GET|HEAD        dashboard/manager/shift .............................................................................................. manager.shiff › User\ManagerController@Shift
  POST            dashboard/manager/shift-schedule ....................................................................... manager.staff.store › User\ManagerController@storeSchedule
  GET|HEAD        dashboard/paramedis .......................................................................................... paramedis.dashboard › User\ParamedisController@index
  POST            dashboard/paramedis/confirm/{id} .................................................................. paramedis.confirm › User\ParamedisController@processHealthCheck
  GET|HEAD        dashboard/paramedis/daily-report .................................................................. daily.report › UserReport\ParamedisReportController@DailyReport
  GET|HEAD        dashboard/paramedis/generate/report .......................................................................... report › UserReport\ParamedisReportController@report
  GET|HEAD        dashboard/paramedis/profile .................................................................................. paramedis.profile › User\ParamedisController@profile
  GET|HEAD        dashboard/paramedis/report .......................................................................... paramedis.report › UserReport\ParamedisReportController@index
  GET|HEAD        dashboard/paramedis/screening/history .............................................. history.paramedis.screening › User\ParamedisController@HistoryOfflineScreening
  GET|HEAD        dashboard/paramedis/screening/offline .............................................. paramedis.screening.offline › Screening\OfflineController@showScreeningOffline
  GET|HEAD        dashboard/paramedis/screening/online ......................................................... paramedis.screeningOnline › User\ParamedisController@ScreeningOnline
  GET|HEAD        dashboard/paramedis/screening/physical/{id} ..................................................... physical.paramedis › User\ParamedisController@PhysicalExamination
  POST            dashboard/paramedis/screening/physical/{id} ....................................................................... physical.store › User\ParamedisController@store
  GET|HEAD        dashboard/paramedis/screening/{id}/detail ................................................. paramedis.questioner.detail › User\ParamedisController@QuestionerDetail
  POST            dashboard/paramedis/{id} ......................................................................... offline.healthcheck › User\ParamedisController@updateHealthCheck
  GET|HEAD        dashboard/profile ................................................................................................ patient.profile › User\PatientController@profile
  GET|HEAD        dashboard/screening/offline .......................................................................... history.screening.offline › Screening\OfflineController@show
  POST            dashboard/screening/offline ........................................................................... screening.offline.store › Screening\OfflineController@store
  GET|HEAD        dashboard/screening/offline/create .......................................................................... screening.offline › Screening\OfflineController@index
  GET|HEAD        dashboard/screening/offline/{id} ................................................................. detail.screening › User\PatientController@DetailScreeningOffline
  GET|HEAD        dashboard/screening/online .................................................................................... screening.online › Screening\OnlineController@index
  GET|HEAD        dashboard/screening/online/create ..................................................................... screening.online.create › Screening\OnlineController@create
  POST            dashboard/screening/online/create ....................................................................... screening.online.store › Screening\OnlineController@store
  GET|HEAD        dashboard/screening/online/payment ........................................................................... screening.payment › Screening\OnlineController@store
  GET|HEAD        dashboard/screening/online/payment/{id} ................................................................... screenings.payment › Screening\OnlineController@payment
  GET|HEAD        docs/api ......................................................................................................................................... scramble.docs.ui
  GET|HEAD        docs/api.json .............................................................................................................................. scramble.docs.document
  POST            email/verification-notification ............................................................ verification.send › Auth\EmailVerificationNotificationController@store
  GET|HEAD        forgot-password ........................................................................................ password.request › Auth\PasswordResetLinkController@create
  POST            forgot-password ........................................................................................... password.email › Auth\PasswordResetLinkController@store
  POST            guest/post ........................................................................................................... guest.post › Screening\GuestController@store
  GET|HEAD        login .......................................................................................................... login › Auth\AuthenticatedSessionController@create
  POST            login ................................................................................................................... Auth\AuthenticatedSessionController@store
  POST            logout ....................................................................................................... logout › Auth\AuthenticatedSessionController@destroy
  PUT             password ......................................................................................................... password.update › Auth\PasswordController@update
  GET|HEAD        print-certificate .................................................................................................... Certificate\PrintController@printCertificate
  GET|HEAD        product ............................................................................................................... product › Ecommerce\ProductController@index
  GET|HEAD        product/cart .......................................................................................................... cart › Ecommerce\ProductController@showCart
  POST            product/cart/{id} .................................................................................................... cart › Ecommerce\ProductController@addToCart
  GET|HEAD        register .......................................................................................................... register › Auth\RegisteredUserController@create
  POST            register ...................................................................................................................... Auth\RegisteredUserController@store
  POST            reset-password .................................................................................................. password.store › Auth\NewPasswordController@store
  GET|HEAD        reset-password/{token} ......................................................................................... password.reset › Auth\NewPasswordController@create
  GET|HEAD        sanctum/csrf-cookie ............................................................................. sanctum.csrf-cookie › Laravel\Sanctum › CsrfCookieController@show
  GET|HEAD        screening-now ................................................................................................... screening.guest › Screening\GuestController@index
  GET|HEAD        send-data .................................................................................................................................. ApiController@sendData
  GET|HEAD        up ................................................................................................................................................................ 
  GET|HEAD        verify-email ......................................................................................... verification.notice › Auth\EmailVerificationPromptController
  GET|HEAD        verify-email/{id}/{hash} ......................................................................................... verification.verify › Auth\VerifyEmailController
  GET|HEAD        {fallbackPlaceholder} .............................................................................................................................................
```
