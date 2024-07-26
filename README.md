# BrainStorm

BrainStorm, kullanıcıların çevrimiçi kurslar oluşturup katılmalarını sağlayan bir dijital eğitim platformudur. Bu platform Java Spring Boot, HTML/CSS/JavaScript, MySQL ve Google Meets API kullanılarak geliştirilmiştir.

## Özellikler

- Kullanıcı ve öğretmen hesapları
- Kurs oluşturma, düzenleme ve silme
- Kurs satın alma ve yorum yapma
- Online ders planlama (Google Meets entegrasyonu)
- Bildirimler ve toplantı takvimi
- Hesap doğrulama

## Teknolojiler

- **Backend**: Java Spring Boot
- **Frontend**: HTML, CSS, JavaScript
- **Veritabanı**: MySQL
- **API**: Google Meets API

## Veritabanı Tabloları

- **comments**: Yorumlar (`comment_id`, `course_id`, `comment`, `rating`, `user_id`)
- **course**: Kurslar (`course_id`, `course_name`, `course_price`, `course_description`, `course_image`, `course_rating`, `course_grade`, `course_lesson`, `teacher_id`)
- **course_schedule**: Ders programı (`id`, `course_id`, `date`, `hours`)
- **expertise**: Uzmanlıklar (`expertise_id`, `expertise_area`, `years_of_experience`, `teacher_id`)
- **meetings**: Toplantılar (`meeting_id`, `meeting_link`, `teacher_id`, `course_id`, `user_id`, `date`, `hour`)
- **notifications**: Bildirimler (`notification_id`, `course_id`, `user_id`, `teacher_id`, `date`, `hour`)
- **taken_course**: Alınan kurslar (`taken_courses_id`, `course_id`, `user_id`)
- **teacher**: Öğretmenler (`teacher_id`, `teacher_name`, `teacher_surname`, `teacher_mail`, `teacher_password`, `teacher_education_level`, `teacher_information`, `verification_token`, `is_used`)
- **user**: Kullanıcılar (`user_id`, `user_name`, `user_surname`, `user_mail`, `user_password`, `user_education_level`, `user_information`, `is_used`)
- **verification_token**: Doğrulama (`token_id`, `token`, `user_id`, `expiry_date`, `is_used`)

## Kurulum

### Gereksinimler

- Java 8+
- MySQL
- Maven
- Google Meets API erişim bilgileri

### Adımlar

1. Depoyu klonlayın:
    ```bash
    git clone https://github.com/gkhancobanoglu/BrainStorm.git
    cd BrainStorm
    ```

2. Veritabanı yapılandırmasını `application.properties` dosyasında güncelleyin:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/brainstorm
    spring.datasource.username=root
    spring.datasource.password=yourpassword
    ```

3. Uygulamayı başlatın:
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

## Kullanım

- Öğrenci veya öğretmen hesabı oluşturun.
- Kursları görüntüleyin, satın alın ve yorum yapın.
- Google Meets API ile online derslere katılın.


