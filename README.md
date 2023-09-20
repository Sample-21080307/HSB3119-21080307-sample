<!DOCTYPE html>
<html><head>
  <title>My Website</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: sans-serif;
      background-color: #f2f2f2;
      background-image: url("binh227.jpg");
      background-size: cover;
      background-position: center;
      transition: background-color 0.5s ease-in-out;
    }

    .header {
  background-color: #4a4242;
  color: #fff;
  padding: 20px;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.header::before {
  content: "";
  position: absolute;
  top: -100%;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.3);
  z-index: -1;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.header:hover::before {
  top: 0;
  opacity: 1;
}

.header h1 {
  font-size: 48px;
  margin: 0;
  position: relative;
  z-index: 2;
  animation: slideInAnimation 1s ease-in-out;
}

@keyframes slideInAnimation {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.header::after {
  content: "";
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.5), transparent);
  pointer-events: none;
  opacity: 0;
  z-index: -1;
  transition: opacity 0.3s ease-in-out;
}

.header:hover::after {
  opacity: 1;
  animation: gradientAnimation 2s linear infinite;
}

@keyframes gradientAnimation {
  0% {
    background-position: 0% 0%;
  }
  100% {
    background-position: -100% 0%;
  }
}


    .content {
      max-width: 800px;
      margin: 50px auto;
      padding: 20px;
      background-color: rgba(255, 255, 255, 0.9);
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      transition: box-shadow 0.5s ease-in-out;
    }
    .content:hover {
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    }

    .about-me {
      display: flex;
      align-items: center;
      margin-bottom: 30px;
      transform-style: preserve-3d;
      animation: flipInAnimation 1s ease-in-out forwards;
    }

    @keyframes flipInAnimation {
      0% {
        opacity: 0;
        transform: rotateY(90deg);
      }
      100% {
        opacity: 1;
        transform: rotateY(0);
      }
    }

    .about-me img {
      width: 200px;
      height: 200px;
      border-radius: 50%;
      object-fit: cover;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      margin-right: 30px;
      transition: transform 0.5s ease-in-out, box-shadow 0.5s ease-in-out;
    }

    .about-me:hover img {
      transform: rotateY(180deg);
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    }

    .about-me .text-right {
      flex: 1;
      transform: rotateY(-90deg);
      transform-origin: right center;
      animation: flipInAnimation 1s ease-in-out forwards;
    }

    .information {
      margin-top: 30px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 20px;
      transform-style: preserve-3d;
      animation: flipInAnimation 1s ease-in-out forwards;
    }

    .information p {
      font-size: 16px;
      line-height: 1.5;
      margin-bottom: 10px;
    }

    .skills {
      margin-top: 30px;
      transform-style: preserve-3d;
      animation: flipInAnimation 1s ease-in-out forwards;
    }

    .skills h2 {
      font-size: 20px;
      margin-bottom: 10px;
    }

    .skills table {
      width: 100%;
      border-collapse: collapse;
    }

    .skills th,
    .skills td {
      padding: 10px;
      border: 1px solid #ccc;
    }

    .skills th {
      background-color: #f2f2f2;
      text-align: left;
    }

    .skills td {
      text-align: center;
    }

  .contact-form {
  margin-top: 30px;
  text-align: center;
}

.contact-form h2 {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333;
}

.contact-form form {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
}

.contact-form .form-group {
  width: 100%;
  margin-bottom: 20px;
}

.contact-form label {
  display: block;
  font-size: 16px;
  margin-bottom: 10px;
  color: #666;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  transition: border-color 0.3s ease-in-out;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border-color: #555;
}

.contact-form textarea {
  resize: vertical;
}

.contact-form button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

.contact-form button:hover {
  background-color: #555;
}

.contact-form .form-group:last-child {
  margin-bottom: 0;
}

.contact-form .form-group::after {
  content: "";
  display: table;
  clear: both;
}

.contact-form .form-group .half-width {
  width: 50%;
  float: left;
  padding-right: 10px;
}

.contact-form .form-group .half-width:last-child {
  padding-right: 0;
}

.contact-form .form-group .full-width {
  width: 100%;
}

@media (max-width: 600px) {
  .contact-form .form-group .half-width {
    width: 100%;
    float: none;
    padding-right: 0;
  }
}
.contact-form {
  margin-top: 30px;
  text-align: center;
  max-width: 500px;
  margin-left: auto;
  margin-right: auto;
}

.contact-form h2 {
  font-size: 24px;
  margin-bottom: 20px;
  color: #333;
}

.contact-form form {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
}

.contact-form .form-group {
  width: 100%;
  margin-bottom: 20px;
}

.contact-form label {
  display: block;
  font-size: 16px;
  margin-bottom: 10px;
  color: #666;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
  transition: border-color 0.3s ease-in-out;
}

.contact-form input:focus,
.contact-form textarea:focus {
  outline: none;
  border-color: #555;
}

.contact-form textarea {
  resize: vertical;
}

.contact-form button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
}

.contact-form button:hover {
  background-color: #555;
}

.contact-form .form-group:last-child {
  margin-bottom: 0;
}

.contact-form .form-group::after {
  content: "";
  display: table;
  clear: both;
}

.contact-form .form-group .half-width {
  width: 50%;
  float: left;
  padding-right: 10px;
}

.contact-form .form-group .half-width:last-child {
  padding-right: 0;
}

.contact-form .form-group .full-width {
  width: 100%;
}

@media (max-width: 600px) {
  .contact-form .form-group .half-width {
    width: 100%;
    float: none;
    padding-right: 0;
  }
}


.contact-form button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease-in-out;
  opacity: 0;
  animation: buttonAnimation 1s ease-in-out forwards;
}

@keyframes buttonAnimation {
  0% {
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

.contact-form button:hover {
  background-color: #555;
}

.contact-form .form-group:nth-child(odd) {
  animation: formFieldAnimationOdd 1s ease-in-out forwards;
}

@keyframes formFieldAnimationOdd {
  0% {
    opacity: 0;
    transform: translateX(100px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.contact-form .form-group:nth-child(even) {
  animation: formFieldAnimationEven 1s ease-in-out forwards;
}

@keyframes formFieldAnimationEven {
  0% {
    opacity: 0;
    transform: translateX(-100px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.contact-form .form-group:nth-child(3n) {
  animation: formFieldAnimation3n 1s ease-in-out forwards;
}

@keyframes formFieldAnimation3n {
  0% {
    opacity: 0;
    transform: translateY(-50px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}



    .photo-gallery {
      margin-top: 30px;
      text-align: center;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      transform-style: preserve-3d;
      animation: flipInAnimation 1s ease-in-out forwards;
    }

    .photo-gallery img {
      display: inline-block;
      width: 200px;
      height: 200px;
      object-fit: cover;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      margin: 10px;
      transition: transform 0.5s ease-in-out, box-shadow 0.5s ease-in-out;
      justify-content: center;
      align-items: center;
      animation: borderAnimation 3s infinite reverse;
    }

    .photo-gallery img:hover {
      transform: rotateY(180deg) scale(1.1);
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    }

    @keyframes flipInAnimation {
      0% {
        transform: rotateY(90deg);
        opacity: 0;
      }
      100% {
        transform: rotateY(0deg);
        opacity: 1;
      }
    }
.social-links {
  margin-top: 30px;
}

.social-links a {
  display: inline-block;
  margin-right: 30px;
}

.social-links img {
  width: 50px;
  height: 50px;
  transition: transform 0.3s ease;
}

.social-links img:hover {
  transform: scale(1.2);
}
  </style>
</head>
<body>
  <div class="header">
      <h1>My Page</h1>
    </div>
    
  

  <div class="content">
    <div class="about-me fade-in">
      <img src="binh profile.jpg" alt="Your Image" />
      <div class="text-right">
        <h2>About Me</h2>
        <p>Chào tất cả mọi người tôi tên là Trịnh Đức Bình, hiện tại tôi đang sinh sống và học tại trường Quản Trị Kinh Doanh của Đại học Quốc Gia Hà Nội. Hiện tại tôi đang làm thêm tại 1 nhà hàng ở Thái Hà. Sở thích của tôi là chơi thể thao và xem phim. Sau đây là website của bản thân tôi. </p>
      </div>
    </div>

    <div class="information fade-in">
      <h2>Information</h2>
      <p>Name: Trịnh Đức Bình</p>
      <p>Age: 20</p>
	  <p>Date of birth: 22/09/2003
	  </p><p>Email: dbinh2323@gmail.com</p>
	  <p>Phone: 0976562288</p>
      <p>Address: Ha Noi</p>
    </div>

    <div class="skills fade-in">
      <h2>Skills</h2>
      <table>
        <tbody><tr>
          <th>Skill</th>
          <th>Description</th>
        </tr>
        <tr>
          <td>Kĩ năng giao tiếp với người nước ngoài</td>
          <td>Tiếng anh hiện nay đang là một trong những ngôn ngữ rất phổ biến và cần thiết trong công việc cũng như là đời sống.Với tấm bằng ielts 6.5 thì tôi có thể giao tiếp với người nước ngoài một cách tự nhiên và có thể nói là theo cách cơ bản nhất</td>
        </tr>
        <tr>
          <td>Kỹ năng quản lý thời gian</td>
          <td>Thời gian chính là một thứ vô cùng quý giá, một khi đã trôi qua thì sẽ không thể lấy lại được. Đối vơi tôi việc quản lí thời gian rất quan trọng,nó giúp tôi kiểm soát được nhiều thứ và hoàn thành được nhiều việc. Vậy nên tôi luôn tìm cách phân bổ một cách đúng nhất và luôn đến đúng giờ những lúc quan trọng.</td>
        </tr>
        <tr>
          <td>Kỹ năng giải quyết vấn đề</td>
          <td>Cuộc sống, công việc mỗi ngày có rất nhiều tình huống bất ngờ xảy ra. Để có thể giải quyết êm đẹp,tôi có khả năng lắng nghe, phân tích, từ đó đưa ra cách xử lý phù hợp.</td>
        </tr>
      </tbody></table>
    </div>

    <div class="contact-form fade-in">
      <div class="container"></div>
      <h2>Contact</h2>
      <form>
        <div class="form-group">
          <label for="name">Your Name</label>
          <input type="text" id="name" name="name" required="" />
        </div>
    
        <div class="form-group">
          <label for="email"> Your Email</label>
          <input type="email" id="email" name="email" required="" />
        </div>
    
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" name="message" required=""></textarea>
        </div>
    
        <button type="submit">Send Message</button>
      </form>
    </div>
    

    <div class="photo-gallery fade-in">
      <h2>Photo Gallery</h2>
      <img src="227.jpg" alt="Photo 1" />
      <img src="229.jpg" alt="Photo 2" />
      <img src="297.jpg" alt="Photo 3" />
    </div>
	<h1>My Social Media</h1>
    <div class="social-links">
      <a href="https://www.facebook.com/profile.php?id=100006412054523" target="_blank"><img src="Facebook.png" alt="Facebook" /></a>
      <a href="https://www.instagram.com/dbinh_23/" target="_blank"><img src="Ins.jpeg" alt="Instagram" /></a>
    </div>
  </div>

  
<div style="text-align:right;position:fixed;z-index:9999999;bottom:0;width:auto;right:1%;cursor:pointer;line-height:0;display:block!important"><a title="Hosted on free web hosting 000webhost.com. Host your own website for FREE." target="_blank" href="https://www.000webhost.com/?utm_source=000webhostapp&amp;utm_campaign=000_logo&amp;utm_medium=website&amp;utm_content=footer_img"><img src="https://cdn.000webhost.com/000webhost/logo/footer-powered-by-000webhost-white2.png" alt="www.000webhost.com" /></a></div><script>function getCookie(t){for(var e=t+"=",n=decodeURIComponent(document.cookie).split(";"),o=0;o<n.length;o++){for(var i=n[o];" "==i.charAt(0);)i=i.substring(1);if(0==i.indexOf(e))return i.substring(e.length,i.length)}return""}getCookie("hostinger")&&(document.cookie="hostinger=;expires=Thu, 01 Jan 1970 00:00:01 GMT;",location.reload());var wordpressAdminBody=document.getElementsByClassName("wp-admin")[0],notification=document.getElementsByClassName("notice notice-success is-dismissible"),hostingerLogo=document.getElementsByClassName("hlogo"),mainContent=document.getElementsByClassName("notice_content")[0];if(null!=wordpressAdminBody&&0<notification.length&&null!=mainContent){var googleFont=document.createElement("link");googleFontHref=document.createAttribute("href"),googleFontRel=document.createAttribute("rel"),googleFontHref.value="https://fonts.googleapis.com/css?family=Roboto:300,400,600,700",googleFontRel.value="stylesheet",googleFont.setAttributeNode(googleFontHref),googleFont.setAttributeNode(googleFontRel);var css="@media only screen and (max-width: 576px) {#main_content {max-width: 320px !important;} #main_content h1 {font-size: 30px !important;} #main_content h2 {font-size: 40px !important; margin: 20px 0 !important;} #main_content p {font-size: 14px !important;} #main_content .content-wrapper {text-align: center !important;}} @media only screen and (max-width: 781px) {#main_content {margin: auto; justify-content: center; max-width: 445px;}} @media only screen and (max-width: 1325px) {.web-hosting-90-off-image-wrapper {position: absolute; max-width: 95% !important;} .notice_content {justify-content: center;} .web-hosting-90-off-image {opacity: 1;}} @media only screen and (min-width: 769px) {.notice_content {justify-content: space-between;} #main_content {margin-left: 5%; max-width: 445px;} .web-hosting-90-off-image-wrapper {position: absolute; display: flex; justify-content: center; width: 50%; margin-left: 45%;}} .web-hosting-90-off-image {max-width: 90%;} .content-wrapper {min-height: 454px; display: flex; flex-direction: column; justify-content: center; z-index: 5} .notice_content {display: flex; align-items: center;} * {-webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale;} .upgrade_button_red_sale{box-shadow: 0 2px 4px 0 rgba(255, 69, 70, 0.2); width: 264px; border: 0; border-radius: 3px; background-color: #FF5C62 !important; padding: 15px 55px !important; font-family: 'Roboto', sans-serif; font-size: 16px; font-weight: 600; color: #ffffff;} .upgrade_button_red_sale:hover{color: #ffffff !important; background: #d10303 !important;}",style=document.createElement("style"),sheet=window.document.styleSheets[0];style.styleSheet?style.styleSheet.cssText=css:style.appendChild(document.createTextNode(css)),document.getElementsByTagName("head")[0].appendChild(style),document.getElementsByTagName("head")[0].appendChild(googleFont);var button=document.getElementsByClassName("upgrade_button_red")[0],link=button.parentElement;link.setAttribute("href","https://www.hostinger.com/hosting-starter-offer?utm_source=000webhost&utm_medium=panel&utm_campaign=000-wp"),link.innerHTML='<button class="upgrade_button_red_sale">Claim Deal</button>',(notification=notification[0]).setAttribute("style","padding-bottom: 0; padding-top: 5px; background-color: #040713; background-size: cover; background-repeat: no-repeat; color: #ffffff; border-left-color: #040713;"),notification.className="notice notice-error is-dismissible";var mainContentHolder=document.getElementById("main_content");mainContentHolder.setAttribute("style","padding: 0;"),hostingerLogo[0].remove();var h1Tag=notification.getElementsByTagName("H1")[0];h1Tag.className="000-h1",h1Tag.innerHTML="Black Friday",h1Tag.setAttribute("style",'color: white; font-family: "Roboto", sans-serif; font-size: 48px; font-weight: 700;');var h2Tag=document.createElement("H2");h2Tag.innerHTML="Up to 90% off 4-year hosting plans + free domain, SSL & DDoS protection",h2Tag.setAttribute("style",'color: white; margin: 10px 0 15px 0; font-family: "Roboto", sans-serif; font-size: 16px; font-weight: 400; line-height: 1;'),h1Tag.parentNode.insertBefore(h2Tag,h1Tag.nextSibling);var paragraph=notification.getElementsByTagName("p")[0];paragraph.innerHTML="$<span style='font-size: 80px;'>2.49</span>/mo",paragraph.setAttribute("style",'font-family: "Roboto", sans-serif; font-size: 48px; font-weight: 700; margin: 0;');var list=notification.getElementsByTagName("UL")[0];list.remove();var org_html=mainContent.innerHTML,new_html='<div class="content-wrapper">'+mainContent.innerHTML+'</div><div class="web-hosting-90-off-image-wrapper"><img class="web-hosting-90-off-image" src="https://cdn.000webhost.com/000webhost/promotions/bf-2022-bottom-banner.png"></div>';mainContent.innerHTML=new_html;var saleImage=mainContent.getElementsByClassName("web-hosting-90-off-image")[0]}</script>
</body></html>
