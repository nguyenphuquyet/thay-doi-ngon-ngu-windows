
<div class='post-title'><h1>Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709</h1></div>
<div class='post-meta'>
<span class='post-author'>ĐỊA CHÍNH CÔNG TRÌNH</span>
<span class='post-timestamp'>October 23, 2017
Monday, October 23, 2017</span>
</div>
<div class='post-social'>
<div class='fb-like' data-action='like' data-href='https://www.diachinhcongtrinh.com/' data-layout='standard' data-show-faces='true' data-size='large'></div>
<span class='printBtn'></span>
<div class='email-popup ma-share' title='Gửi email cho tác giả'></div>
<div class='btn-popup' role='alert'>
<div class='btn-popup-container'>
<h2>gửi email cho tác giả</h2><br/><br/>
<form name='contact-form'>
<div class='blanterinput'>
<input class='validate' id='ContactForm1_contact-form-name' name='name' required='' type='text' value=''/>
<span class='highlight'></span>
<span class='bar'></span>
<label><i class='fa fa-user'></i>&nbsp;&nbsp;Họ tên</label>
</div>
<div class='blanterinput'>
<input class='validate' id='ContactForm1_contact-form-email' name='email' required='' type='email' value=''/>
<span class='highlight'></span>
<span class='bar'></span>
<label><i class='fa fa-envelope'></i>&nbsp;&nbsp;Email của bạn</label>
</div>
<div class='blanterinput'>
<textarea class='validate' cols='25' id='ContactForm1_contact-form-email-message' name='email-message' required='' rows='5'></textarea>
<span class='highlight'></span>
<span class='bar'></span>
<label><i class='fa fa-microphone'></i>&nbsp;&nbsp;Nội dung</label>
</div>
<input id='ContactForm1_contact-form-submit' type='button' value='Gửi email'/>
<div id='ContactForm1_contact-form-error-message'>
</div>
<div id='ContactForm1_contact-form-success-message'>
</div>
</form>
<a class='btn-popup-close img-replace'></a>
</div>
</div>
</div>
</div>
<div class='klw-new-content'>
<div class='knc-menu-nav'>
<div class='kmn-wrapper'>
<div class='kmnw-content'>
<div class='kc-item kc-home'><a class='icon-kch' href='https://www.diachinhcongtrinh.com/' title='Home'></a></div>
<div class='kc-item kc-facebook icon-kcf' id='feedBtn'><a class='icon-kcf' href='http://www.facebook.com/sharer.php?u=https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html&title=Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709' title='Đăng bài viết này lên dòng thời gian của bạn'></a></div>
<div class='kc-item kc-messenger' id='sendBtn'><a class='icon-kcm' title='Gửi bài viết này cho bạn bè'></a></div>
</div>
</div>
</div>
<p class='post-metaDescription'>
</p>
<div class='related-post' id='related-post'>
<script>
      var labelArray = ["rebuild"];
      var relatedPostConfig = {
        homePage: "/",   
        numPosts: 3,
        containerId: "related-post",
        callBack: function() {}
      };
    </script>
</div>
</div>
<div class='post-body' id='post-body'>
<p>Trong bài viết này tôi sẽ hướng dẫn các bạn cách tích hợp gói ngôn ngữ khác ngôn ngữ mặc định của bộ cài&nbsp;Windows 10 version 1709 vẫn thường sử dụng bộ cài tiếng Anh (en-US). Cách tích hợp ngôn ngữ bằng phương pháp sử dụng lệnh trong Cmd. Các bạn lưu ý trong gói ngôn ngữ tải về tôi chỉ để 6 gói ngôn ngữ chính thông dụng bao gồm ngôn ngữ cho WinPE (boot.wim) Windows (install.wim) và Windows RE (winre.wim) và với phương pháp thực hiện bên dưới tôi sẽ tích hợp tiếng Trung zh-cn<br /><a name='more'></a><br /><div class="separator" style="clear: both; text-align: center;"><a href="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="763" data-original-width="1024" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png" /></a></div><br /><b>Để thực hiện bạn cần có:</b><br /><ul><li><a href="http://www.blogthuthuatwin10.com/2017/10/moi-tai-ve-windows-10-fall-creators-update-version-1709-chinh-thuc-tu-msdn.html" target="_blank">Bộ cài Windows 10 version 1709</a></li><li><a href="https://www.fshare.vn/file/Z6JZ1W6VK12Y" target="_blank">Gói ngôn ngữ</a></li></ul><b>Cách thực hiện</b><br /><br />Lưu ý trong bài viết này tôi sử dụng bộ cài Win 10 64 bit, nếu làm 32 bit đổi x64 thành x86<br /><br />Bước 1: Gói ngôn ngữ tải về giải nén vào một ổ đĩa nào còn trống dung lượng ví dụ như ổ E chẳng hạn.<br /><br />Bước 2: Khởi chạy Cmd bằng quyền admin<br /><br />Bước 3: Tạo mới các thư mục cần thiết, sử dụng các lệnh sau để tạo mới<br /><br />Tạo thư mục <b>win10_x64</b> lưu bộ cài Windows<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p1" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p1"><br />md E:\win10_x64<br /><br /></pre><br />Tạo thư mục <b>images</b> lưu tập tin gắn kết install.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p2" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p2"><br />md E:\images<br /><br /></pre><br />Tạo thư mục <b>winpe</b> mount tập tin boot.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p3" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p3"><br />md E:\mount\winpe<br /><br /></pre><br />Tạo thư mục <b>windows</b> mount install.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p4" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p4"><br />md E:\mount\windows<br /><br /></pre><br />Tạo thư mục <b>winre</b> mount winre.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p5" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p5"><br />md E:\mount\winre<br /><br /></pre><br />Bước 3: Mount bộ cài Windows ra ổ ảo (chuột phải iso chọn mount) chẳng hạn ổ ảo sau khi mount có ký tự ổ đĩa là I<br /><br />Bước 4: Copy tất cả trong ổ ảo I vào thư mục lưu bộ cài win10_x64<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p6" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p6"><br />xcopy I:\ E:\win10_x64 /s /i<br /><br /></pre><br />Bước 5: Xem thông tin tập tin install.wim trong thư mục sources của thư mục win10_x64 bao gồm mấy phiên bản<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p7" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p7"><br />Dism /Get-ImageInfo /ImageFile:E:\win10_x64\sources\install.wim<br /><br /></pre><br />Ví dụ với tập tin install.wim bao gồm 9 phiên bản<br /><br /><div class="separator" style="clear: both; text-align: center;"><a href="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjAZCB7mxRhy8OLp7JPiY-gp4iNrrpD45lP6jatqLqRnKJ2Y1ASuCvjUyajxVzMhyphenhyphenRxpL5ZqggD4sDYjSY2G0ebl934zLqBwNIVBd6FXMAfq0KkdgtvvL83bxsm_cEatBAwWCp68MIbePbs/s1600/2017-10-18_21-29-01.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="725" data-original-width="444" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjAZCB7mxRhy8OLp7JPiY-gp4iNrrpD45lP6jatqLqRnKJ2Y1ASuCvjUyajxVzMhyphenhyphenRxpL5ZqggD4sDYjSY2G0ebl934zLqBwNIVBd6FXMAfq0KkdgtvvL83bxsm_cEatBAwWCp68MIbePbs/s1600/2017-10-18_21-29-01.png" /></a></div><br />Bước 6: Xuất phiên bản Pro trong install.wim ra install.wim mới và lưu trong thư mục images<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p8" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p8"><br />Dism /Export-Image /SourceImageFile:E\win10_x64\sources\install.wim /SourceIndex:8 /DestinationImageFile:E:\images\install.wim<br /><br /></pre><br />Bước 7: Mout ba tập tin gắn kết boot.wim, install.wim và winre.wim<br /><br />- Mount tập tin boot.wim trong thư mục sources của thư mục win10_x64 vào thư mục winpe của thư mục mount<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p9" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p9"><br />Dism /mount-image /imagefile:E:\win10_x64\sources\boot.wim /index:2 /mountdir:E:\mount\winpe<br /><br /></pre><br />- Mount tập tin install.wim trong thư mục images vào thư mục windows của thư mục mount<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p10" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p10"><br />Dism /Mount-Image /ImageFile:E:\images\install.wim /Index:1 /MountDir:E:\mount\windows<br /><br /></pre><br />- Mount tập tin winre.wim trong thư mục recovery theo đường dẫn windows\system32\ của thư mục windows đã mount vào thư mục winre của thư mục mount<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p11" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p11"><br />Dism /Mount-Image /ImageFile:E:\mount\windows\windows\system32\recovery\winre.wim /Index:1 /MountDir:E:\mount\winre<br /><br /></pre><br />Bước 8: Tích hợp gói ngôn ngữ<br /><br />- Tích hợp ngôn ngữ cho winpe (boot.wim)<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p12" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p12"><br />Dism /Image:E:\mount\winpe /Add-Package /Packagepath:E:\langpacks\langpacks_winpe\x64\zh-cn<br /><br /></pre><br />- Tích hợp ngôn ngữ cho winre (winre.wim)<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p13" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p13"><br />Dism /Image:E:\mount\winre /Add-Package /Packagepath:E:\langpacks\langpacks_winre\x64\zh-cn<br /><br /></pre><br />- Tích hợp ngôn ngữ cho Windows (insatll.wim)<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p14" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p14"><br />Dism /Image:E:\mount\windows /Add-Package /Packagepath:E:\langpacks\langpacks_windows\x64\zh-cn<br /><br /></pre><br />Bước 9: Tạo tập tin lang.ini mới thay thế cho tập tin lang.ini cũ lưu trong thư mục sources của thư mục lưu bộ cài win10_x64<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p15" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p15"><br />Dism /image:E:\mount\windows /gen-langINI /distribution:E:\win10_x64<br /><br /></pre><br />Bước 10: Copy tập tin lang.ini mới tạo vào thư mục sources của thư mục winpe<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p16" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p16"><br />copy E:\win10_x64\sources\lang.ini E:\mount\winpe\sources\lang.ini<br /><br /></pre><br />nhấn Y xác nhận<br /><br />Bước 10: Unmount 3 tập tin boot.wim, winre.wim và install.wim<br /><br />- Unmount tập tin boot.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p17" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p17"><br />Dism /Unmount-Image /MountDir:E:\mount\winpe /Commit<br /><br /></pre><br />- Unmount tập tin winre.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p18" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p18"><br />Dism /Unmount-Image /MountDir:E:\mount\winre /Commit<br /><br /></pre><br />- Unmount tập tin install.wim<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p19" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p19"><br />Dism /Unmount-Image /MountDir:E:\mount\windows /Commit<br /><br /></pre><br />Bước 11: Xóa tập tin install.wim gốc trong thư mục sources của bộ cài trong thư mục win10_x64<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p20" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p20"><br />del E:\win10_x64\sources\install.wim /s<br /><br /></pre><br />Bước 12: Di chuyển tập tin install.wim mới trong thư mục images vào thư mục sources của thư mục win10_x64<br /><br /><div class="codeHeader"> <a class="copy-text" data-clipboard-target="#p21" href="javascript:void(0);"><i class="fa fa-files-o"></i> Copy</a></div><pre class="code" id="p21"><br />move E:\images\install.wim E:\win10_x64\sources\install.wim<br /><br /></pre><br />Khi tích hợp xong bạn có thể copy tất cả trong thư mục win10_x64 vào usb đã định dạng FAT32 để cài đặt hoặc nếu bạn muốn tạo iso mới có thể sử dụng UltraISO hoặc phần mềm tương tự. Bạn cũng có thể sử dụng cmd để tạo Windows ISO boot với cả hai chuẩn UEFI boot và Legacy boot, xem bài viết chi tiết tại <b><a href="http://www.blogthuthuatwin10.com/2016/12/su-dung-cmd-e-tao-windows-iso-boot-voi.html" target="_blank">đây</a></b>.</p>
<div id='ads_Code'>
<script>
var mql = window.matchMedia('screen and (max-width: 960px)');if (mql.matches){
document.write("<ins class='adsbygoogle' data-ad-client='ca-pub-7197786739659219' data-ad-format='fluid' data-ad-layout='in-article' style='display:block; text-align:center;margin-top:15px'></ins>");
};
</script>
</div>
<script>
//<![CDATA[ 
var keyword_collect = [ "admin","adsense","AIO","bảo mật","batch","Mapping Gis","Blog","blogger","blogspot","cài đặt","cập nhật","Chơi Blog","code","Cortana","command","dữ liệu","dữ liệu cấu trúc","đăng nhập","điều kiện","fix lỗi","full disk","game","ghost","hệ thống","kích hoạt","kiếm tiền","khởi động","label","lock screen","Microsoft","menu","mới nhất","multiboot","office 2016","iso","phần mềm","phục hồi","Tài liệu","AutoCad","quản trị viên","registry","services","update","recovery","winre","reset","sao lưu","SEO","Seo","Seo label","máy tính","quảng cáo","start menu","sysprep","System Apps","tài liệu","template","template blogspot","theme","Đo đạc","thủ thuật blogspot","Thủ thuật blogspot","tin tức","ứng dụng","video","Windows","Windows Apps","Windows 10","Windows 8.1","Windows 7","win pe","slide","Windows RE","Recovery","google","slider","Facebook","tags","tìm kiếm","scripts","script","powershell","WIN AIO" ] 

function makeKeywordForPost(mKF_id) {
  var content;
  var isDOM = (navigator.appName.match("Microsoft Internet Explorer") || navigator.appName.match("MSIE")) ? false : true;
  if (isDOM) {
    content = document.getElementById(mKF_id).textContent;
  } else {
    content = document.getElementById(mKF_id).innerText;
  }
  var str = "";
  var link1 = "/search?q=";
  var link2 = "&max-results=10";
  for (var j = 0; j < keyword_collect.length; j++) {
    if (content.indexOf(" " + keyword_collect[j] + " ") != -1) {
      str += '<a href="' + link1 + encodeURIComponent(keyword_collect[j]) + link2 + '">' + keyword_collect[j] + '</a>';
    }
  }
  str = (str != "") ? keyword_text + str : keyword_text + "no keyword";
  document.write(str);
}
//]]></script>
<div class='keywords'>
<script>//<![CDATA[ 
keyword_text ="<b>Tags: </b>";
window.onLoad = makeKeywordForPost("post-body");
//]]></script>
</div>
<div id='ads_Code'>
<script>
var mql = window.matchMedia('screen and (max-width: 960px)');if (mql.matches){
document.write("<ins class='adsbygoogle' data-ad-client='ca-pub-7197786739659219' data-ad-format='fluid' data-ad-layout='in-article' style='display:block; text-align:center;margin-top:15px'></ins>");
};
</script>
</div>
</div>
<script type='application/ld+json'> {
    "@context": "http://schema.org",
    "@type": "NewsArticle",
    "mainEntityOfPage": {
      "@type": "WebPage",
      "@id": "https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html"
    },
    "headline": "Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709",
    "description": "",
    "image": {
      "@type": "ImageObject",
      "url": "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png",
      "width": 720,
      "height": 480
    },
    "datePublished": "2017-10-23T23:17:00+07:00",
    "dateModified": "2017-10-23T23:17:00+07:00",
    "author": {
      "@type": "Person",
      "name": "ĐỊA CHÍNH CÔNG TRÌNH"
    },
    "publisher": {
      "@type": "Organization",
      "name": "DIACHINHCONGTRINH.COM",
      "logo": {
        "@type": "ImageObject",
        "url": "https://3.bp.blogspot.com/-e8hXBRehutU/WlbeZ3CxA8I/AAAAAAAARtI/eLYb--ZwqlQrF9A3Sz66YZx6qr72xcShACLcBGAs/s1600/logo.png"
      }
    }
  } </script>
<div class='post-footer'>
<span class='post-backlinks post-comment-link'>
</span>
<div class='social-sharing-widgets'>
<span class='social-sharing-text'>Chia sẻ nội dung này:</span>
<a class='social-widget' href='http://www.facebook.com/sharer.php?u=https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html&title=Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709' onclick='window.open(this.href, "_blank", "height=630,width=840"); return false;' target='_blank' title='Share to Facebook'><span class='facebook-icon social-icon'></span></a>
<a class='social-widget' href='https://plus.google.com/share?url=https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html&title=Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709' onclick='window.open(this.href, "_blank", "height=430,width=640"); return false;' target='_blank' title='Chia sẻ lên Google+'><span class='google-plus-icon social-icon'></span>
</a>
<a class='social-widget' href='http://twitter.com/share?url=https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html&title=Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709' onclick='window.open(this.href, "_blank", "height=430,width=640"); return false;' target='_blank' title='Share to X'><span class='twitter-icon social-icon'></span></a>
<a class='social-widget' href='http://www.linkedin.com/shareArticle?url=https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html&title=Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709' onclick='window.open(this.href, "_blank", "height=430,width=640"); return false;' target='_blank' title='Chia sẻ lên Linkedin'><span class='linkedin-icon social-icon'></span></a>
<div class='dropdown social-sharing-text'>
<a class='dropdown-link'>Thêm</a>
<div class='dropdown-container'>
<ul>
<li class='dropdown-container_sub2'></li>
<li><a class='copy-link' onclick='CopyLink()' style='cursor: pointer;' title='Nhận liên kết'>Nhận liên kết</a></li>
<li><a class="rss-follow" href="//www.blogger.com/follow-blog.g?blogID=4562796330339503496" onclick="javascript:window.open(this.href, &quot;bloggerPopup&quot;, &quot;toolbar=0,location=0,statusbar=1,menubar=0,scrollbars=yes,width=590,height=540&quot;); return false;" rel="nofollow" target="blank" title="Theo dõi Blog này">Theo dõi blog</a></li>
<li><a class='rss-follow' href='//feedburner.google.com/fb/a/mailverify?uri=blogthuthuatwin10' onclick='javascript:window.open(this.href, "bloggerPopup", "toolbar=0,location=0,statusbar=1,menubar=0,scrollbars=yes,width=590,height=540"); return false;' rel='nofollow' target='blank' title='Nhận bài mới qua email'>Đăng ký</a></li>
</ul>
</div>
</div>
</div>
<div class='fb-comments'>
<div class='fb-comments' data-href='https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html' data-numposts='5' data-width='100%'></div>
</div>
<div id='related-posts'>
<h3>CÙNG CHUYÊN MỤC</h3>
<script>
      var currentposturl="https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html";
      var maxresults=12; 
	  printRelatedLabels_thumbs();
    </script>
</div>
</div>
<div class='clear'></div>
</article>
<div class='comments' id='comments'>
<a name='comments'></a>
<div class='commenter'>
</div>
<div class='comments-content'>
<div id='comment-holder'>
<!--Can't find substitution for tag [post.commentHtml]-->
</div>
</div>
<p class='comment-footer'>
<!--Can't find substitution for tag [post.noNewCommentsText]-->
</p>
<div id='backlinks-container'>
<div id='Blog1_backlinks-container'>
</div>
</div>
</div>
</div>
<div class='widget HTML' data-version='2' id='HTML5'>
<div class='widget-content'>
<!-- Nguồn cấp -->
</div>
</div><div class='widget PopularPosts' data-version='1' id='PopularPosts1'>
<h3><span>Phổ biến trong tuần</span></h3>
<div class='widget-content popular-posts'>
<ul>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/01/bo-cai-microstation-v8i-full-va-huong.html' title='Bộ cài MicroStation V8i full và hướng dẫn cài đặt'>
<img alt='Bộ cài MicroStation V8i full và hướng dẫn cài đặt' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgVtNagrRmmrNdxdvK4rbQbA191HXVsUa60xLJeIIeW3cH_DyRFK-M3rMTDJGC5sZBuC1gw2KR1keyXUD7gcA6xV6UC6dVakbstI16AClzeEIeNQuMwVsyGWF-a2VLhzjwiQ0oUCYo3_lk/w72-h72-p-k-no-nu/2018-01-20_151842.png'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/01/bo-cai-microstation-v8i-full-va-huong.html' title='Bộ cài MicroStation V8i full và hướng dẫn cài đặt'>Bộ cài MicroStation V8i full và hướng dẫn cài đặt</a></div>
<div class='item-snippet'>   &#160; Bentley MicroStation V8i  là một chương trình CAD được thiết kế đồ họa mạnh mẽ so với các phiên bản cũ. MicroStation V8i tương thích vớ...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/06/khac-phuc-loi-font-chu-ban-o-tren.html' title='Khắc phục lỗi Font chữ bản đồ trên MicroSation V8i'>
<img alt='Khắc phục lỗi Font chữ bản đồ trên MicroSation V8i' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhcIVPwn6htDSs6Xb6PuvDdCDzzn3XSgAEsO4f6G118D11UYiHwSyAdsZFGcuifTG32jCEza0fM_nugXVD29BDepdeve63_Mti2dpM438lZNbd5NJ9tNEUyJ8RiUPYGWcXMyBP7LJpg7MM/w72-h72-p-k-no-nu/2018-06-08_210557.jpg'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/06/khac-phuc-loi-font-chu-ban-o-tren.html' title='Khắc phục lỗi Font chữ bản đồ trên MicroSation V8i'>Khắc phục lỗi Font chữ bản đồ trên MicroSation V8i</a></div>
<div class='item-snippet'> &#160; &#160; &#160; Khi mở bản đồ, hồ sơ kỹ thuật bằng MicroSation bị lỗi font chữ?&#160;Đừng lo nắng, mình xin hướng dẫn sửa lỗi font chữ trên&#160; MicroSation V...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/01/phan-mem-cai-at-microsation-se-v7-full.html' title='Phần mềm Microsation SE V7 Full tích hợp Famis TT25 mới nhất và IrasB, IrasC, GEOVEC'>
<img alt='Phần mềm Microsation SE V7 Full tích hợp Famis TT25 mới nhất và IrasB, IrasC, GEOVEC' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhegqyn21tg3QIVfOhKEpsHKuUXZcnuk8gd-eaHaU3PywecyUE0aQXKrcM8n9VaJGPXUGmu7CTGdE207S0wp-tQ_BMRNzOHTQy1VKI5zczxSrp0hWVQAlZyFdlSTm1izS7VgMV8GB6f5M0/w72-h72-p-k-no-nu/2018-01-03_213341.png'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/01/phan-mem-cai-at-microsation-se-v7-full.html' title='Phần mềm Microsation SE V7 Full tích hợp Famis TT25 mới nhất và IrasB, IrasC, GEOVEC'>Phần mềm Microsation SE V7 Full tích hợp Famis TT25 mới nhất và IrasB, IrasC, GEOVEC</a></div>
<div class='item-snippet'>     &#160;&#160;  &#160; &#160; &#160;  &#160; &#160; &#160; MicroStation &#160; là một&#160;phần mềm&#160;giúp thiết kế (CAD) được sản xuất và phân phối bởi&#160;Bentley Systems [1] . MicroStation c...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/12/download-global-mapper.html' title='Download Global Mapper Full'>
<img alt='Download Global Mapper Full' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj05wk4hRW9r6PnBqyC1xH_MsJ08-QmfDYNNPlb-EAlxnu2C7eQtI8edGjYYiN7vsgCMUfAV6iOq_Jq1eQZ3ptVKnmllzByhISEiU0X2LOWHJnWuY_NFUSUHaDYRIFOn29F7KdE_C0DU3c/w72-h72-p-k-no-nu/ddct.jpg'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/12/download-global-mapper.html' title='Download Global Mapper Full'>Download Global Mapper Full</a></div>
<div class='item-snippet'>   &#160; &#160; &#160; Global Mapper là ứng dụng có khả năng tạo bản đồ, công cụ cho phép chỉnh sửa, tạo và xóa các thông tin bản đồ. Đặc biệt Global Mapp...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/07/bo-cai-microsation-v8iss4081109832-va.html' title='Bộ cài MicroSation V8i.SS4.08.11.09.832 và hướng dẫn cài đặt'>
<img alt='Bộ cài MicroSation V8i.SS4.08.11.09.832 và hướng dẫn cài đặt' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgeCas1lFomGTLZa9YDRkuVVFMX-8sqG3urgHFCOlN22LSdcrxUQkTJlbiEf60wI-51SA7gFq3SgDuqqti8nn0FXgJlx1roPSbxmWSOSe-7s8IM2g3Zgs7nTQj9vV7sHrpcCd11GgkDA_Q/w72-h72-p-k-no-nu/2018-07-03_121825.jpg'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/07/bo-cai-microsation-v8iss4081109832-va.html' title='Bộ cài MicroSation V8i.SS4.08.11.09.832 và hướng dẫn cài đặt'>Bộ cài MicroSation V8i.SS4.08.11.09.832 và hướng dẫn cài đặt</a></div>
<div class='item-snippet'>              I) Bộ cài MicroSation V8i.SS4.08.11.09.832: &#160;                       II) Hướng dẫn cài đặt:&#160;       &#160; &#160; Lưu ý: Khi cài đặt cần đ...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2019/02/cac-loi-thuong-gap-trong-microsation.html' title='Các lỗi thường gặp trong Microsation'>
<img alt='Các lỗi thường gặp trong Microsation' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhiUZUbE5PsbYSc_OHaV1aWoLw3dvspRRN1hDMSnubpYZc8mA9eu8YfaJMGfjHuTJQETaD25cChmhblxvhx3Oun_tnSH_o1iYomzJ2FxfbMEAEBY0V8eoxTa0ompIawPEsjiW7nPO8gJMs/w72-h72-p-k-no-nu/2019-02-14_082510.png'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2019/02/cac-loi-thuong-gap-trong-microsation.html' title='Các lỗi thường gặp trong Microsation'>Các lỗi thường gặp trong Microsation</a></div>
<div class='item-snippet'>   1. Báo lỗi Error:  hresult=8007000e  &quot;Can&#39;t open file&quot;  &quot;Not enough storage is available to complete this operation...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2019/03/huong-dan-chuyen-ban-ve-len-google.html' title='Hướng dẫn chuyển bản vẽ lên Google Earth bằng MicroSation V8i - Đưa bản vẽ MicroSation, AutoCad, MapInfo lên Google Earth bằng phần mềm Global Mapper'>
<img alt='Hướng dẫn chuyển bản vẽ lên Google Earth bằng MicroSation V8i - Đưa bản vẽ MicroSation, AutoCad, MapInfo lên Google Earth bằng phần mềm Global Mapper' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiPCJwSiJBkANYt5Iep84Zx5XLsXqI_vJoCH2P1eRbhMEd7nQZ7JhPGB1X5Gcj32Xv4ntv4BmcCPYrwHY7ZMNmDiOG4ttiadnNt_HHbLsFet-Qy_STddRZbumB9dTZ9f4OEDkAd-LTCWKo/w72-h72-p-k-no-nu/2019-03-27_015444.png'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2019/03/huong-dan-chuyen-ban-ve-len-google.html' title='Hướng dẫn chuyển bản vẽ lên Google Earth bằng MicroSation V8i - Đưa bản vẽ MicroSation, AutoCad, MapInfo lên Google Earth bằng phần mềm Global Mapper'>Hướng dẫn chuyển bản vẽ lên Google Earth bằng MicroSation V8i - Đưa bản vẽ MicroSation, AutoCad, MapInfo lên Google Earth bằng phần mềm Global Mapper</a></div>
<div class='item-snippet'>    1. Cài phần mềm Google Earth Pro:          2. Hướng dẫn&#160;đưa bản vẽ MicroSation V8i lên Google Earth:   +) Cài VN2000 vào MicroSation V8i...</div>
</div>
<div style='clear: both;'></div>
</li>
<li>
<div class='item-content'>
<div class='item-thumbnail'>
<a href='https://www.diachinhcongtrinh.com/2018/01/sua-loi-font-famis-va-tmvmap-tren.html' title='Sửa lỗi font Famis và TMV.Map trên MicroSation nhanh chóng đơn giản'>
<img alt='Sửa lỗi font Famis và TMV.Map trên MicroSation nhanh chóng đơn giản' border='0' src='https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgzr2207QdHtBNnwny5p7-wp4SsBqub4Sm70y2oq6Ap3ceALZkv6AFIdsCNKjZ8SnMi83n91iW-nqH-PMIWUPawwktmzcORgDyjNBZCe80fqcyCsQNdiVNaHbMkEF_4Vq2pgQJX-2kTp04/w72-h72-p-k-no-nu/2018-01-02_212821.png'/>
</a>
</div>
<div class='item-title'><a href='https://www.diachinhcongtrinh.com/2018/01/sua-loi-font-famis-va-tmvmap-tren.html' title='Sửa lỗi font Famis và TMV.Map trên MicroSation nhanh chóng đơn giản'>Sửa lỗi font Famis và TMV.Map trên MicroSation nhanh chóng đơn giản</a></div>
<div class='item-snippet'> &#160; Sau khi cài Famis và TMV.Map thường xảy ra lỗi Font trên thanh menu .             Hướng dẫn sửa lỗi Font: Để chạy chương trình sửa lỗi fo...</div>
</div>
<div style='clear: both;'></div>
</li>
</ul>
</div>
</div><div class='widget HTML' data-version='2' id='HTML6'>
<div class='widget-content'>
<!-- Nguồn cấp -->
</div>
</div><div class='widget HTML' data-version='2' id='HTML7'>
<h3 class='recent-posts'><a href='https://www.diachinhcongtrinh.com/search?&max-results=10' title='Bài đăng gần đây'>Tin Tức</a></h3>
<div id='recent-posts'>
<script>
var numposts = 6;
var showpostthumbnails = true;
var showcommentnum = false;
var showpostdate = false;
var showpostsummary = true;
var numchars = 150;
</script>
<script src='/feeds/posts/default?published&alt=json-in-script&callback=labelthumbs' type='text/javascript'></script>
<div class='clear'></div>
</div>
</div>
</div>
<div class='clear'></div>
</div>
<!-- End Article -->
<!-- Sidebar -->
<div class='sidebar-wrapper'>
<div class='breadcrumbs-right'>
<a class='lien-he' href='/p/contact.html' title='Liên hệ'>Liên hệ</a><a class='gop-y' href='/p/tro-giup-windows-10.html' title='Trợ giúp Windows 10'>Trợ giúp</a>
</div>
<div class='sidebar section' id='sidebar' name='Sidebar'><div class='widget HTML' data-version='2' id='HTML19'>
<div class='widget-content'>
<div class='vka-wrapper'>
<input class='vka-checkbox' id='vkaCheckbox' type='checkbox'/>
<label class='vka' for='vkaCheckbox'>
<i class='icon-cps-vka-menu'></i>
</label>
<div class='vka-wheel'>
<!--a class='vka-action vka-action-1' href='' rel='nofollow' target='_blank' title='Tìm cửa hàng'> <div class='vka-button vka-button-1'><i class='icon-cps-local'/></div> </a-->
<!--a<a class='vka-action vka-action-2' href='tel:0777922218' rel='nofollow' title='Gọi trực tiếp'> -->
<div class='vka-button vka-button-2'><i class='icon-cps-phone'></i></div>

<a class='vka-action vka-action-3' href='https://www.messenger.com/t/diachinhcongtrinh.com1' rel='nofollow' target='_blank' title='Chat Facebook'>
<div class='vka-button vka-button-3'><i class='icon-cps-facebook'></i></div>
</a>
<a class='vka-action vka-action-4' href=' ' rel='nofollow' target='_blank' title='Chat Zalo'>
<div class='vka-button vka-button-4'><i class='icon-cps-chat-zalo'></i></div>
</a>
</div>
</div>
<style>
.vka-wrapper {
    position: fixed;
    bottom: 5px;
    right: 0;
    z-index: 9999999;
}
  
.vka-checkbox {
    display: none !important;
}
  
.vka {
    width: 60px;
    max-width: unset;
    height: 60px;
    display: flex !important;
    justify-content: center;
    align-items: center;
    margin: 0;
    border-radius: 50%;
    background: #c31d1d;
    box-shadow: 0 3px 6px rgb(0 0 0 / 16%), 0 3px 6px rgb(0 0 0 / 23%);
    position: absolute;
    right: 10px;
    bottom: 10px;
    z-index: 1000;
    overflow: hidden;
    transform: rotate( 0deg );
    -webkit-transition: all .15s cubic-bezier(.15,.87,.45,1.23);
    transition: all .15s cubic-bezier(.15,.87,.45,1.23);
}
  
.vka-checkbox:checked~.vka {
    -webkit-transition: all .15s cubic-bezier(.15,.87,.45,1.23);
    transition: all .15s cubic-bezier(.15,.87,.45,1.23);
    width: 30px;
    height: 30px;
    right: 26px;
    bottom: 35px;
}
  
[class*=icon-cps-] {
    display: inline-block;
    vertical-align: middle;
    background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAANoAAAB1CAYAAAAoV//gAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6ODVFMzM1MDcwNDAyMTFFQ0I0OTJBMEYxN0VGQ0ExRTMiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6ODVFMzM1MDgwNDAyMTFFQ0I0OTJBMEYxN0VGQ0ExRTMiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo4NUUzMzUwNTA0MDIxMUVDQjQ5MkEwRjE3RUZDQTFFMyIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo4NUUzMzUwNjA0MDIxMUVDQjQ5MkEwRjE3RUZDQTFFMyIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/Phh/T5sAACNZSURBVHja7F0HuFXF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)!important;
    background-repeat: no-repeat;
    background-size: 148px;
}
  
.icon-cps-vka-menu {
    width: 50px;
    height: 50px;
    margin: 0 !important;
    background-size: 200px;
    background-position: -155px 0;
}
.vka-checkbox:checked~.vka .icon-cps-vka-menu {
    width: 20px;
    height: 20px;
    margin: 0;
    background-size: 100px;
    background-position: -79px -29px;
}
  
.vka-wheel {
    position: absolute;
    bottom: 15px;
    right: 18px;
    transform: scale(0);
    transform-origin: bottom right;
    transition: all .3s ease;
    z-index: 12;
}
  
.vka-checkbox:checked~.vka-wheel {
    transform: scale(1);
}
  
.vka-wheel .vka-action {
    display: flex;
    align-items: center;
    font-size: 14px;
    font-weight: 700;
    color: #fff;
    position: absolute;
    text-decoration: none;
}
  
.vka-wheel .vka-action:hover {
    transform: scale(1.1);
}
  
.vka-wheel .vka-action-1 {
    bottom: 225px;
    right: 0;
}
  
.vka-button {
    width: 45px;
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
    float: left;
    padding: 4px;
    border-radius: 50%;
    background: #0f1941;
    box-shadow: 0 1px 3px rgb(0 0 0 / 12%), 0 1px 2px rgb(0 0 0 / 24%);
    font-size: 24px;
    color: White;
    transition: all 1s ease;
    overflow: hidden;
}
  
.icon-cps-local {
    width: 30px;
    height: 30px;
    background-position: -5px -43px;
}
 
.icon-cps-mail {
    width: 30px;
    height: 30px;
    background-position: -8px -5px;
}
  
.icon-cps-facebook {
    width: 30px;
    height: 30px;
    background-position: -80px -43px;
}
  
.vka-wheel .vka-button-1 {
    background: #0f9d58;
}
  
.vka-wheel .vka-action-2 {
    bottom: 170px;
    right: 0;
}
  
.vka-wheel .vka-button-2 {
    background: #fb0;
}
  
.icon-cps-phone {
    width: 30px;
    height: 30px;
    background-position: -42px -45px;
}
  
.vka-wheel .vka-action-3 {
    right: 0;
    bottom: 115px;
    cursor: pointer;
}
  
.vka-wheel .vka-button-3 {
    background: #006AFF;
}
  
.vka-wheel .vka-action-4 {
    right: 0;
    bottom: 60px;
}
  
.vka-wheel .vka-button-4 {
    background: #2f82fc;
}
  
.icon-cps-chat-zalo {
    width: 30px;
    height: 30px;
    background-position: -47px -5px;
    background-size: 155px;
}
  
.hidden {
    display: none!important;
}
  
.align-items-center {
    -ms-flex-align: center!important;
    align-items: center!important;
    -ms-flex-pack: distribute!important;
    justify-content: space-around!important;
    display: -ms-flexbox!important;
    display: flex!important;
    -webkit-box-align: center!important;
    -ms-flex-align: center!important;
    align-items: center!important;
}
  
  
.vka-checkbox:not(:checked)~.vka {
    animation-name: zoom;
    -webkit-animation-name: zoom;
    animation-delay: 0s;
    -webkit-animation-delay: 0s;
    animation-duration: 1.5s;
    -webkit-animation-duration: 1.5s;
    animation-iteration-count: infinite;
    -webkit-animation-iteration-count: infinite;
    cursor: pointer;
    box-shadow: 0 0 0 0 #c31d1d;
}
  
@-webkit-keyframes tada {
    0% {
        -webkit-transform: scale(1);
        transform: scale(1)
    }
  
    10%,20% {
        -webkit-transform: scale(.9) rotate(-3deg);
        transform: scale(.9) rotate(-3deg)
    }
  
    30%,50%,70%,90% {
        -webkit-transform: scale(1.1) rotate(3deg);
        transform: scale(1.1) rotate(3deg)
    }
  
    40%,60%,80% {
        -webkit-transform: scale(1.1) rotate(-3deg);
        transform: scale(1.1) rotate(-3deg)
    }
  
    100% {
        -webkit-transform: scale(1) rotate(0);
        transform: scale(1) rotate(0)
    }
}
  
@keyframes tada {
    0% {
        -webkit-transform: scale(1);
        -ms-transform: scale(1);
        transform: scale(1)
    }
  
    10%,20% {
        -webkit-transform: scale(.9) rotate(-3deg);
        -ms-transform: scale(.9) rotate(-3deg);
        transform: scale(.9) rotate(-3deg)
    }
  
    30%,50%,70%,90% {
        -webkit-transform: scale(1.1) rotate(3deg);
        -ms-transform: scale(1.1) rotate(3deg);
        transform: scale(1.1) rotate(3deg)
    }
  
    40%,60%,80% {
        -webkit-transform: scale(1.1) rotate(-3deg);
        -ms-transform: scale(1.1) rotate(-3deg);
        transform: scale(1.1) rotate(-3deg)
    }
  
    100% {
        -webkit-transform: scale(1) rotate(0);
        -ms-transform: scale(1) rotate(0);
        transform: scale(1) rotate(0)
    }
}
  
@-webkit-keyframes zoom {
    0% {
        transform: scale(.9)
    }
  
    70% {
        transform: scale(1);
        box-shadow: 0 0 0 15px transparent
    }
  
    100% {
        transform: scale(.9);
        box-shadow: 0 0 0 0 transparent
    }
}
  
@keyframes zoom {
    0% {
        transform: scale(.9)
    }
  
    70% {
        transform: scale(1);
        box-shadow: 0 0 0 15px transparent
    }
  
    100% {
        transform: scale(.9);
        box-shadow: 0 0 0 0 transparent
    }
}
</style>
</div>
</div><div class='widget HTML' data-version='2' id='HTML21'>
<div class='widget-content'>
<div id="fb-root"></div>
<script>(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = "//connect.facebook.net/vi_VN/sdk.js#xfbml=1&version=v2.10&appId=152370588675388";
  fjs.parentNode.insertBefore(js, fjs);
}(document, 'script', 'facebook-jssdk'));</script>
<div class="fb-page" data-href="https://www.facebook.com/diachinhcongtrinh.com1/" data-tabs="timeline" data-small-header="false" data-adapt-container-width="true" data-hide-cover="false" data-show-facepile="true"><blockquote cite="https://www.facebook.com/diachinhcongtrinh.com1/" class="fb-xfbml-parse-ignore"><a href="https://www.diachinhcongtrinh.com/">Địa Chính Công Trình</a></blockquote></div>
</div>
</div><div class='widget HTML' data-version='2' id='HTML12'>
<div class='widget-content'>
<style>
#fbox-background {
display: none;
background: rgba(0,0,0,0.8);
width: 100%;
height: 100%;
position: fixed;
top: 0;
left: 0;
z-index: 99999;
}
#fbox-close {
width: 100%;
height: 100%;
}
#fbox-display {
background: #eaeaea;
border: 5px solid #3a5795;
width: 340px;
height: 230px;
position: absolute;
top: 32%;
left: 37%;
-webkit-border-radius: 5px;
-moz-border-radius: 5px;
border-radius: 5px;
}
#fbox-button {
float: right;
cursor: pointer;
position: absolute;
right: 0px;
top: 0px;
}
#fbox-button:before {
content: "CLOSE";
padding: 5px 8px;
background: #3a5795;
color: #eaeaea;
font-weight: bold;
font-size: 10px;
font-family: Tahoma;
}
#fbox-link,#fbox-link a.visited,#fbox-link a,#fbox-link a:hover {
color: #aaaaaa;
font-size: 9px;
text-decoration: none;
text-align: center;
padding: 5px;
}
</style>
<script type='text/javascript'>
//<![CDATA[
jQuery.cookie = function (key, value, options) {
// key and at least value given, set cookie...
if (arguments.length > 1 && String(value) !== "[object Object]") {
options = jQuery.extend({}, options);
if (value === null || value === undefined) {
options.expires = -1;
}
if (typeof options.expires === 'number') {
var days = options.expires, t = options.expires = new Date();
t.setDate(t.getDate() + days);
}
value = String(value);
return (document.cookie = [
encodeURIComponent(key), '=',
options.raw ? value : encodeURIComponent(value),
options.expires ? '; expires=' + options.expires.toUTCString() : '', // use expires attribute, max-age is not supported by IE
options.path ? '; path=' + options.path : '',
options.domain ? '; domain=' + options.domain : '',
options.secure ? '; secure' : ''
].join(''));
}
// key and possibly options given, get cookie...
options = value || {};
var result, decode = options.raw ? function (s) { return s; } : decodeURIComponent;
return (result = new RegExp('(?:^|; )' + encodeURIComponent(key) + '=([^;]*)').exec(document.cookie)) ? decode(result[1]) : null;
};
//]]>
</script>
<script type='text/javascript'>
jQuery(document).ready(function($){
if($.cookie('popup_facebook_box') != 'yes'){
$('#fbox-background').delay(5000).fadeIn('medium');
$('#fbox-button, #fbox-close').click(function(){
$('#fbox-background').stop().fadeOut('medium');
});
}
$.cookie('popup_facebook_box', 'yes', { path: '/', expires: 7 });
});
</script>
<div id='fbox-background'>
<div id='fbox-close'>
</div>
<div id='fbox-display'>
<div id='fbox-button'>
</div>
<iframe allowtransparency='true' frameborder='0' scrolling='no' src='//www.facebook.com/plugins/likebox.php?
href=https://www.facebook.com/diachinhcongtrinh.com1/&width=402&height=255&colorscheme=light&show_faces=true&show_border=false&stream=false&header=false'
style='border: none; overflow: hidden; background: #fff; width: 250px; height: 150px;'></iframe>
<div id="fbox-link">Powered by <a style="padding-left: 0px;" href="https://www.diachinhcongtrinh.com/" rel="nofollow">Like Fanpage theo dõi bài viết Địa Chính Công Trình</a></div>
</div>
</div>
</div>
</div>
<div class='widget ContactForm' data-version='1' id='ContactForm1'>
</div></div>
</div>
<!-- End Sidebar -->
<div class='clear'></div>
</div>
<!-- End Main Wrapper -->
<!-- Footer Wrapper -->
<div class='footer-wrapper'>
<div class='ads no-items section' id='Ads-7' name='Reponsive ads (Footer)'>
</div>
</div>
<div class='ads-banner'>
<div class='ads-left no-items section' id='banner-trai' name='Ads 90x720 (Banner Left)'>
</div>
<div class='ads-right no-items section' id='banner-phai' name='Ads 90x720 (Banner Right)'>
</div>
</div>
<!-- End Footer Wrapper -->
</section>
<!-- End Container -->
<!-- Footer -->
<footer id='footer'>
<div class='footer-container'>
<div class='footer-top'>
<span class='footer-top-text'>Kết nối với Địa Chính Công Trình trên:</span>
<a href='https://plus.google.com/u/0/106698840804938779740' rel='nofollow' target='blank' title='Theo dõi Google+'><span class='google-plus-icon social-icon'></span></a>
<a href='https://twitter.com/Windows_1Office' rel='nofollow' target='blank' title='Theo dõi Twitter'><span class='twitter-icon social-icon'></span></a>
<a href='https://www.facebook.com/pg/diachinhcongtrinh/posts/?ref=page_internal' rel='nofollow' target='blank' title='Like Fanpage'><span class='facebook-icon social-icon'></span></a>
<a href='https://www.linkedin.com/in/nguy%E1%BB%85n-tu%E1%BA%A5n-0332b5154/detail/recent-activity/' rel='nofollow' target='blank' title='Theo dõi Linkedin'><span class='linkedin-icon social-icon'></span></a>
</div>
<div class='box2'>
<div class='footer section' id='footer1' name='LinkList 1'><div class='widget LinkList' data-version='2' id='LinkList1'>
<h3 class='title'>
Liên Kết Link
</h3>
<div class='widget-content'>
<ul>
<li><a href='https://www.facebook.com/groups/778107945586650/' title='☛ Groups'>&#9755; Groups</a></li>
<li><a href='https://www.facebook.com/diachinhcongtrinh/' title='☛ Fanpage'>&#9755; Fanpage</a></li>
<li><a href='https://www.nhasachgiaoducvn.com/' title='Nhà sách giáo dục vn'>Nhà sách giáo dục vn</a></li>
<li><a href='https://www.hoalanrung.org/' title='Hoa Lan Rừng'>Hoa Lan Rừng</a></li>
<li><a href='https://www.xusohoa.com/' title='Hoa Hồng'>Hoa Hồng</a></li>
</ul>
</div>
</div></div>
<div class='footer section' id='footer2' name='LinkList 2'><div class='widget LinkList' data-version='2' id='LinkList2'>
<h3 class='title'>
Chuyên mục khác
</h3>
<div class='widget-content'>
<ul>
<li><a href='/search/label/phan-mem?&amp;max-results=10' title='Phần mềm Windows'>Phần mềm Windows</a></li>
<li><a href='/search/label/microsoft-office?&amp;max-results=10' title='Microsoft Office'>Microsoft Office</a></li>
<li><a href='/search/label/windows-iso?&amp;max-results=10' title='Windows ISO'>Windows ISO</a></li>
<li><a href='/search/label/ghost?&amp;max-results=10' title='GHOST'>GHOST</a></li>
<li><a href='/search/label/game?&amp;max-results=10' title='Games'>Games</a></li>
</ul>
</div>
</div></div>
<div class='footer section' id='footer3' name='LinkList 3'><div class='widget LinkList' data-version='2' id='LinkList5'>
<h3 class='title'>
Cộng Đồng
</h3>
<div class='widget-content'>
<ul>
<li><a href='https://www.facebook.com/groups/778107945586650/?ref=bookmarks'>&#9755; Tham gia cộng đồng Địa Chính Công Trình</a></li>
<li><a href='https://www.diachinhcongtrinh.com/2018/08/huong-dan-tai-file-tu-ia-chinh-cong.html'>Hướng dẫn tải file từ Địa Chính Công Trình  https://www.diachinhcongtrinh.com/ </a></li>
</ul>
</div>
</div>
</div>
<div class='footer section' id='footer4' name='LinkList 4'><div class='widget HTML' data-version='2' id='HTML20'>
<div class='widget-content'>
<a href="//www.dmca.com/Protection/Status.aspx?ID=a8890120-d764-4398-9a59-b5a8fea18401" title="DMCA.com Protection Status" class="dmca-badge"> <img src ="https://images.dmca.com/Badges/dmca_protected_sml_120b.png?ID=a8890120-d764-4398-9a59-b5a8fea18401"  alt="DMCA.com Protection Status" /></a>  <script src="https://images.dmca.com/Badges/DMCABadgeHelper.min.js"> </script>
</div>
</div>
</div>
<div class='clear'></div>
</div>
<div class='footer-bottom'>
<div class='footer-bottom-left'>
<a href='/p/about-us.html' title='Giới thiệu'>Giới thiệu</a>&nbsp;&nbsp;&nbsp;&nbsp;
        <a href='/p/contact.html' title='Liên hệ'>Liên hệ</a>&nbsp;&nbsp;&nbsp;&nbsp;
        <a href='/p/tro-giup-windows-10.html' title='Trợ giúp'>Trợ giúp</a>&nbsp;&nbsp;&nbsp;&nbsp;
        <a href='/p/sitemap.html' title='Sitemap'>Sitemap</a>
</div>
<div class='footer-bottom-right'>
<a href='https://www.diachinhcongtrinh.com/' title='Địa Chính Công Trình'>Địa Chính Công Trình</a>
</div>
</div>
</div>
</footer>
<!-- End Footer -->
<div class='MD-StoTop' title='Lên đầu trang'></div>
<script>
//<![CDATA[
$(document).ready(function() {
  $(".toggleMenu").click(function() {
    $(".dropdowns").toggleClass("shows")
  }), $(".showsearch,#showsearch2").click(function() {
    $("#search-box").toggleClass("shows")
  })
  $('#PopularPosts1 .item-thumbnail img,#PopularPosts2 .item-thumbnail img').attr('src', function(i, src) {
    return src.replace('w72-h72-p-k-no-nu', 's1600')
  })
});

$(function() {
  $.fn.scrollToTop = function() {
    $(this).hide().removeAttr("href"), "0" != $(window).scrollTop() && $(this).fadeIn("slow");
    var o = $(this);
    $(window).scroll(function() {
      "0" == $(window).scrollTop() ? $(o).fadeOut("slow") : $(o).fadeIn("slow")
    }), $(this).click(function() {
      $("html, body").animate({
        scrollTop: 0
      }, "slow")
    })
  }
}), $(function() {
  $(".MD-StoTop").scrollToTop()
});
$(function() {
  $(".gb_fa.gb_ga").mousemove(function() {
    $(".gb_fa").css("overflow", "auto")
  }), $("#header-wrapper,.main-wrapper,#footer").mousemove(function() {
    $(".gb_fa").css("overflow", "hidden")
  })
});
$(document).ready(function(){var dayName=new Array("Chủ nhật","Thứ hai","Thứ ba","Thứ tư","Thứ năm","Thứ sáu","Thứ bảy");var monName=new Array("1","2","3","4","5","6","7","8","9","10","11","12");var now=new Date();var str_time=dayName[now.getDay()]+', '+now.getDate()+'/'+monName[now.getMonth()]+'/'+now.getFullYear()+' '+now.getHours()+':'+now.getMinutes()+' GMT+7';$('.tm').html(str_time);});
(function($){var e={topSpacing:0,bottomSpacing:0,className:'is-sticky',center:false},$window=$(window),$document=$(document),sticked=[],windowHeight=$window.height(),scroller=function(){var a=$window.scrollTop(),documentHeight=$document.height(),dwh=documentHeight-windowHeight,extra=(a>dwh)?dwh-a:0;for(var i=0;i<sticked.length;i++){var s=sticked[i],elementTop=s.stickyWrapper.offset().top,etse=elementTop-s.topSpacing-extra;if(a<=etse){if(s.currentTop!==null){s.stickyElement.css('position','').css('top','').removeClass(s.className);s.currentTop=null}}else{var b=documentHeight-s.elementHeight-s.topSpacing-s.bottomSpacing-a-extra;if(b<0){b=b+s.topSpacing}else{b=s.topSpacing}if(s.currentTop!=b){s.stickyElement.css('position','fixed').css('top',b).addClass(s.className);s.currentTop=b}}}},resizer=function(){windowHeight=$window.height()};if(window.addEventListener){window.addEventListener('scroll',scroller,false);window.addEventListener('resize',resizer,false)}else if(window.attachEvent){window.attachEvent('onscroll',scroller);window.attachEvent('onresize',resizer)}$.fn.sticky=function(d){var o=$.extend(e,d);return this.each(function(){var a=$(this);if(o.center)var b="margin-left:auto;margin-right:auto;";stickyId=a.attr('id');a.wrapAll('<div id="'+stickyId+'StickyWrapper" style="'+b+'"></div>').css('width',a.width());var c=a.outerHeight(),stickyWrapper=a.parent();stickyWrapper.css('width',a.outerWidth()).css('height',c).css('clear',a.css('clear'));sticked.push({topSpacing:o.topSpacing,bottomSpacing:o.bottomSpacing,stickyElement:a,currentTop:null,stickyWrapper:stickyWrapper,elementHeight:c,className:o.className})})}})(jQuery);
$(document).ready(function(){
  $("#HTML15").sticky({topSpacing:0,bottomSpacing:680})
});
//]]>
</script>
<div id='fb-root'></div>
<script>
//<![CDATA[
$(document).ready(function(){$(".dropdown").each(function(){var t=$(this);$(".dropdown-link",t).click(function(e){return e.preventDefault(),$div=$(".dropdown-container",t),$div.toggle(),$(".dropdown-container").not($div).hide(),!1})}),$("html").click(function(){$(".dropdown-container").hide()})})
jQuery(document).ready(function(e){e(".cd-popup-trigger").on("click",function(i){i.preventDefault(),e(".cd-popup").addClass("is-visible")}),e(".cd-popup").on("click",function(i){(e(i.target).is(".cd-popup-close")||e(i.target).is(".cd-popup"))&&(i.preventDefault(),e(this).removeClass("is-visible"))}),e(".cd-popup").on("click",function(i){(e(i.target).is(".clickbutton")||e(i.target).is(".cd-popup"))&&(i.preventDefault(),e(this).removeClass("is-visible"))}),e(document).keyup(function(i){"27"==i.which&&e(".cd-popup").removeClass("is-visible")})});
jQuery(document).ready(function(e){e(".email-popup").on("click",function(p){p.preventDefault(),e(".btn-popup").addClass("is-visible")}),e(".btn-popup").on("click",function(p){(e(p.target).is(".btn-popup-close")||e(p.target).is(".btn-popup"))&&(p.preventDefault(),e(this).removeClass("is-visible"))}),e(document).keyup(function(p){"27"==p.which&&e(".btn-popup").removeClass("is-visible")})});
!function(t){if("object"==typeof exports&&"undefined"!=typeof module)module.exports=t();else if("function"==typeof define&&define.amd)define([],t);else{var e;e="undefined"!=typeof window?window:"undefined"!=typeof global?global:"undefined"!=typeof self?self:this,e.Clipboard=t()}}(function(){var t;return function e(t,n,o){function i(a,c){if(!n[a]){if(!t[a]){var s="function"==typeof require&&require;if(!c&&s)return s(a,!0);if(r)return r(a,!0);var l=new Error("Cannot find module '"+a+"'");throw l.code="MODULE_NOT_FOUND",l}var u=n[a]={exports:{}};t[a][0].call(u.exports,function(e){var n=t[a][1][e];return i(n?n:e)},u,u.exports,e,t,n,o)}return n[a].exports}for(var r="function"==typeof require&&require,a=0;a<o.length;a++)i(o[a]);return i}({1:[function(t,e){var n=t("matches-selector");e.exports=function(t,e,o){for(var i=o?t:t.parentNode;i&&i!==document;){if(n(i,e))return i;i=i.parentNode}}},{"matches-selector":5}],2:[function(t,e){function n(t,e,n,i,r){var a=o.apply(this,arguments);return t.addEventListener(n,a,r),{destroy:function(){t.removeEventListener(n,a,r)}}}function o(t,e,n,o){return function(n){n.delegateTarget=i(n.target,e,!0),n.delegateTarget&&o.call(t,n)}}var i=t("closest");e.exports=n},{closest:1}],3:[function(t,e,n){n.node=function(t){return void 0!==t&&t instanceof HTMLElement&&1===t.nodeType},n.nodeList=function(t){var e=Object.prototype.toString.call(t);return void 0!==t&&("[object NodeList]"===e||"[object HTMLCollection]"===e)&&"length"in t&&(0===t.length||n.node(t[0]))},n.string=function(t){return"string"==typeof t||t instanceof String},n.fn=function(t){var e=Object.prototype.toString.call(t);return"[object Function]"===e}},{}],4:[function(t,e){function n(t,e,n){if(!t&&!e&&!n)throw new Error("Missing required arguments");if(!a.string(e))throw new TypeError("Second argument must be a String");if(!a.fn(n))throw new TypeError("Third argument must be a Function");if(a.node(t))return o(t,e,n);if(a.nodeList(t))return i(t,e,n);if(a.string(t))return r(t,e,n);throw new TypeError("First argument must be a String, HTMLElement, HTMLCollection, or NodeList")}function o(t,e,n){return t.addEventListener(e,n),{destroy:function(){t.removeEventListener(e,n)}}}function i(t,e,n){return Array.prototype.forEach.call(t,function(t){t.addEventListener(e,n)}),{destroy:function(){Array.prototype.forEach.call(t,function(t){t.removeEventListener(e,n)})}}}function r(t,e,n){return c(document.body,t,e,n)}var a=t("./is"),c=t("delegate");e.exports=n},{"./is":3,delegate:2}],5:[function(t,e){function n(t,e){if(i)return i.call(t,e);for(var n=t.parentNode.querySelectorAll(e),o=0;o<n.length;++o)if(n[o]==t)return!0;return!1}var o=Element.prototype,i=o.matchesSelector||o.webkitMatchesSelector||o.mozMatchesSelector||o.msMatchesSelector||o.oMatchesSelector;e.exports=n},{}],6:[function(t,e){function n(t){var e;if("INPUT"===t.nodeName||"TEXTAREA"===t.nodeName)t.focus(),t.setSelectionRange(0,t.value.length),e=t.value;else{t.hasAttribute("contenteditable")&&t.focus();var n=window.getSelection(),o=document.createRange();o.selectNodeContents(t),n.removeAllRanges(),n.addRange(o),e=n.toString()}return e}e.exports=n},{}],7:[function(t,e){function n(){}n.prototype={on:function(t,e,n){var o=this.e||(this.e={});return(o[t]||(o[t]=[])).push({fn:e,ctx:n}),this},once:function(t,e,n){function o(){i.off(t,o),e.apply(n,arguments)}var i=this;return o._=e,this.on(t,o,n)},emit:function(t){var e=[].slice.call(arguments,1),n=((this.e||(this.e={}))[t]||[]).slice(),o=0,i=n.length;for(o;i>o;o++)n[o].fn.apply(n[o].ctx,e);return this},off:function(t,e){var n=this.e||(this.e={}),o=n[t],i=[];if(o&&e)for(var r=0,a=o.length;a>r;r++)o[r].fn!==e&&o[r].fn._!==e&&i.push(o[r]);return i.length?n[t]=i:delete n[t],this}},e.exports=n},{}],8:[function(e,n,o){!function(i,r){if("function"==typeof t&&t.amd)t(["module","select"],r);else if("undefined"!=typeof o)r(n,e("select"));else{var a={exports:{}};r(a,i.select),i.clipboardAction=a.exports}}(this,function(t,e){"use strict";function n(t){return t&&t.__esModule?t:{"default":t}}function o(t,e){if(!(t instanceof e))throw new TypeError("Cannot call a class as a function")}var i=n(e),r="function"==typeof Symbol&&"symbol"==typeof Symbol.iterator?function(t){return typeof t}:function(t){return t&&"function"==typeof Symbol&&t.constructor===Symbol?"symbol":typeof t},a=function(){function t(t,e){for(var n=0;n<e.length;n++){var o=e[n];o.enumerable=o.enumerable||!1,o.configurable=!0,"value"in o&&(o.writable=!0),Object.defineProperty(t,o.key,o)}}return function(e,n,o){return n&&t(e.prototype,n),o&&t(e,o),e}}(),c=function(){function t(e){o(this,t),this.resolveOptions(e),this.initSelection()}return t.prototype.resolveOptions=function(){var t=arguments.length<=0||void 0===arguments[0]?{}:arguments[0];this.action=t.action,this.emitter=t.emitter,this.target=t.target,this.text=t.text,this.trigger=t.trigger,this.selectedText=""},t.prototype.initSelection=function(){this.text?this.selectFake():this.target&&this.selectTarget()},t.prototype.selectFake=function(){var t=this,e="rtl"==document.documentElement.getAttribute("dir");this.removeFake(),this.fakeHandlerCallback=function(){return t.removeFake()},this.fakeHandler=document.body.addEventListener("click",this.fakeHandlerCallback)||!0,this.fakeElem=document.createElement("textarea"),this.fakeElem.style.fontSize="12pt",this.fakeElem.style.border="0",this.fakeElem.style.padding="0",this.fakeElem.style.margin="0",this.fakeElem.style.position="absolute",this.fakeElem.style[e?"right":"left"]="-9999px",this.fakeElem.style.top=(window.pageYOffset||document.documentElement.scrollTop)+"px",this.fakeElem.setAttribute("readonly",""),this.fakeElem.value=this.text,document.body.appendChild(this.fakeElem),this.selectedText=(0,i["default"])(this.fakeElem),this.copyText()},t.prototype.removeFake=function(){this.fakeHandler&&(document.body.removeEventListener("click",this.fakeHandlerCallback),this.fakeHandler=null,this.fakeHandlerCallback=null),this.fakeElem&&(document.body.removeChild(this.fakeElem),this.fakeElem=null)},t.prototype.selectTarget=function(){this.selectedText=(0,i["default"])(this.target),this.copyText()},t.prototype.copyText=function(){var t=void 0;try{t=document.execCommand(this.action)}catch(e){t=!1}this.handleResult(t)},t.prototype.handleResult=function(t){t?this.emitter.emit("success",{action:this.action,text:this.selectedText,trigger:this.trigger,clearSelection:this.clearSelection.bind(this)}):this.emitter.emit("error",{action:this.action,trigger:this.trigger,clearSelection:this.clearSelection.bind(this)})},t.prototype.clearSelection=function(){this.target&&this.target.blur(),window.getSelection().removeAllRanges()},t.prototype.destroy=function(){this.removeFake()},a(t,[{key:"action",set:function(){var t=arguments.length<=0||void 0===arguments[0]?"copy":arguments[0];if(this._action=t,"copy"!==this._action&&"cut"!==this._action)throw new Error('Invalid "action" value, use either "copy" or "cut"')},get:function(){return this._action}},{key:"target",set:function(t){if(void 0!==t){if(!t||"object"!==("undefined"==typeof t?"undefined":r(t))||1!==t.nodeType)throw new Error('Invalid "target" value, use a valid Element');if("copy"===this.action&&t.hasAttribute("disabled"))throw new Error('Invalid "target" attribute. Please use "readonly" instead of "disabled" attribute');if("cut"===this.action&&(t.hasAttribute("readonly")||t.hasAttribute("disabled")))throw new Error('Invalid "target" attribute. You can\'t cut text from elements with "readonly" or "disabled" attributes');this._target=t}},get:function(){return this._target}}]),t}();t.exports=c})},{select:6}],9:[function(e,n,o){!function(i,r){if("function"==typeof t&&t.amd)t(["module","./clipboard-action","tiny-emitter","good-listener"],r);else if("undefined"!=typeof o)r(n,e("./clipboard-action"),e("tiny-emitter"),e("good-listener"));else{var a={exports:{}};r(a,i.clipboardAction,i.tinyEmitter,i.goodListener),i.clipboard=a.exports}}(this,function(t,e,n,o){"use strict";function i(t){return t&&t.__esModule?t:{"default":t}}function r(t,e){if(!(t instanceof e))throw new TypeError("Cannot call a class as a function")}function a(t,e){if(!t)throw new ReferenceError("this hasn't been initialised - super() hasn't been called");return!e||"object"!=typeof e&&"function"!=typeof e?t:e}function c(t,e){if("function"!=typeof e&&null!==e)throw new TypeError("Super expression must either be null or a function, not "+typeof e);t.prototype=Object.create(e&&e.prototype,{constructor:{value:t,enumerable:!1,writable:!0,configurable:!0}}),e&&(Object.setPrototypeOf?Object.setPrototypeOf(t,e):t.__proto__=e)}function s(t,e){var n="data-clipboard-"+t;return e.hasAttribute(n)?e.getAttribute(n):void 0}var l=i(e),u=i(n),f=i(o),d=function(t){function e(n,o){r(this,e);var i=a(this,t.call(this));return i.resolveOptions(o),i.listenClick(n),i}return c(e,t),e.prototype.resolveOptions=function(){var t=arguments.length<=0||void 0===arguments[0]?{}:arguments[0];this.action="function"==typeof t.action?t.action:this.defaultAction,this.target="function"==typeof t.target?t.target:this.defaultTarget,this.text="function"==typeof t.text?t.text:this.defaultText},e.prototype.listenClick=function(t){var e=this;this.listener=(0,f["default"])(t,"click",function(t){return e.onClick(t)})},e.prototype.onClick=function(t){var e=t.delegateTarget||t.currentTarget;this.clipboardAction&&(this.clipboardAction=null),this.clipboardAction=new l["default"]({action:this.action(e),target:this.target(e),text:this.text(e),trigger:e,emitter:this})},e.prototype.defaultAction=function(t){return s("action",t)},e.prototype.defaultTarget=function(t){var e=s("target",t);return e?document.querySelector(e):void 0},e.prototype.defaultText=function(t){return s("text",t)},e.prototype.destroy=function(){this.listener.destroy(),this.clipboardAction&&(this.clipboardAction.destroy(),this.clipboardAction=null)},e}(u["default"]);t.exports=d})},{"./clipboard-action":8,"good-listener":4,"tiny-emitter":7}]},{},[9])(9)}),$(function(){new Clipboard(".copy-text")});
function copyTextToClipboard(e){var t=document.createElement("textarea");t.style.position="fixed",t.style.top=0,t.style.left=0,t.style.width="2em",t.style.height="2em",t.style.padding=0,t.style.border="none",t.style.outline="none",t.style.boxShadow="none",t.style.background="transparent",t.value=e,document.body.appendChild(t),t.select();try{document.execCommand("copy"),alert("Đã sao chép liên kết!")}catch(o){alert("Không thể sao chép liên kết!")}document.body.removeChild(t)}function CopyLink(){copyTextToClipboard(location.href)}
function setTooltip(t,e){t.tooltip("hide").attr("data-original-title",e).tooltip("show")}function hideTooltip(t){setTimeout(function(){t.tooltip("hide")},1e3)}if("undefined"==typeof jQuery)throw new Error("Bootstrap's JavaScript requires jQuery");+function(t){"use strict";var e=t.fn.jquery.split(" ")[0].split(".");if(e[0]<2&&e[1]<9||1==e[0]&&9==e[1]&&e[2]<1||e[0]>3)throw new Error("Bootstrap's JavaScript requires jQuery version 1.9.1 or higher, but lower than version 4")}(jQuery),+function(t){"use strict";function e(e){return this.each(function(){var o=t(this),n=o.data("bs.tooltip"),s="object"==typeof e&&e;!n&&/destroy|hide/.test(e)||(n||o.data("bs.tooltip",n=new i(this,s)),"string"==typeof e&&n[e]())})}var i=function(t,e){this.type=null,this.options=null,this.enabled=null,this.timeout=null,this.hoverState=null,this.$element=null,this.inState=null,this.init("tooltip",t,e)};i.VERSION="3.3.7",i.TRANSITION_DURATION=150,i.DEFAULTS={animation:!0,placement:"top",selector:!1,template:'<div class="tooltip" role="tooltip"><div class="tooltip-arrow"></div><div class="tooltip-inner"></div></div>',trigger:"hover focus",title:"",delay:0,html:!1,container:!1,viewport:{selector:"body",padding:0}},i.prototype.init=function(e,i,o){if(this.enabled=!0,this.type=e,this.$element=t(i),this.options=this.getOptions(o),this.$viewport=this.options.viewport&&t(t.isFunction(this.options.viewport)?this.options.viewport.call(this,this.$element):this.options.viewport.selector||this.options.viewport),this.inState={click:!1,hover:!1,focus:!1},this.$element[0]instanceof document.constructor&&!this.options.selector)throw new Error("`selector` option must be specified when initializing "+this.type+" on the window.document object!");for(var n=this.options.trigger.split(" "),s=n.length;s--;){var r=n[s];if("click"==r)this.$element.on("click."+this.type,this.options.selector,t.proxy(this.toggle,this));else if("manual"!=r){var l="hover"==r?"mouseenter":"focusin",a="hover"==r?"mouseleave":"focusout";this.$element.on(l+"."+this.type,this.options.selector,t.proxy(this.enter,this)),this.$element.on(a+"."+this.type,this.options.selector,t.proxy(this.leave,this))}}this.options.selector?this._options=t.extend({},this.options,{trigger:"manual",selector:""}):this.fixTitle()},i.prototype.getDefaults=function(){return i.DEFAULTS},i.prototype.getOptions=function(e){return e=t.extend({},this.getDefaults(),this.$element.data(),e),e.delay&&"number"==typeof e.delay&&(e.delay={show:e.delay,hide:e.delay}),e},i.prototype.getDelegateOptions=function(){var e={},i=this.getDefaults();return this._options&&t.each(this._options,function(t,o){i[t]!=o&&(e[t]=o)}),e},i.prototype.enter=function(e){var i=e instanceof this.constructor?e:t(e.currentTarget).data("bs."+this.type);return i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i)),e instanceof t.Event&&(i.inState["focusin"==e.type?"focus":"hover"]=!0),i.tip().hasClass("in")||"in"==i.hoverState?void(i.hoverState="in"):(clearTimeout(i.timeout),i.hoverState="in",i.options.delay&&i.options.delay.show?void(i.timeout=setTimeout(function(){"in"==i.hoverState&&i.show()},i.options.delay.show)):i.show())},i.prototype.isInStateTrue=function(){for(var t in this.inState)if(this.inState[t])return!0;return!1},i.prototype.leave=function(e){var i=e instanceof this.constructor?e:t(e.currentTarget).data("bs."+this.type);return i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i)),e instanceof t.Event&&(i.inState["focusout"==e.type?"focus":"hover"]=!1),i.isInStateTrue()?void 0:(clearTimeout(i.timeout),i.hoverState="out",i.options.delay&&i.options.delay.hide?void(i.timeout=setTimeout(function(){"out"==i.hoverState&&i.hide()},i.options.delay.hide)):i.hide())},i.prototype.show=function(){var e=t.Event("show.bs."+this.type);if(this.hasContent()&&this.enabled){this.$element.trigger(e);var o=t.contains(this.$element[0].ownerDocument.documentElement,this.$element[0]);if(e.isDefaultPrevented()||!o)return;var n=this,s=this.tip(),r=this.getUID(this.type);this.setContent(),s.attr("id",r),this.$element.attr("aria-describedby",r),this.options.animation&&s.addClass("fade");var l="function"==typeof this.options.placement?this.options.placement.call(this,s[0],this.$element[0]):this.options.placement,a=/\s?auto?\s?/i,p=a.test(l);p&&(l=l.replace(a,"")||"top"),s.detach().css({top:0,left:0,display:"block"}).addClass(l).data("bs."+this.type,this),this.options.container?s.appendTo(this.options.container):s.insertAfter(this.$element),this.$element.trigger("inserted.bs."+this.type);var h=this.getPosition(),c=s[0].offsetWidth,u=s[0].offsetHeight;if(p){var f=l,d=this.getPosition(this.$viewport);l="bottom"==l&&h.bottom+u>d.bottom?"top":"top"==l&&h.top-u<d.top?"bottom":"right"==l&&h.right+c>d.width?"left":"left"==l&&h.left-c<d.left?"right":l,s.removeClass(f).addClass(l)}var v=this.getCalculatedOffset(l,h,c,u);this.applyPlacement(v,l);var g=function(){var t=n.hoverState;n.$element.trigger("shown.bs."+n.type),n.hoverState=null,"out"==t&&n.leave(n)};t.support.transition&&this.$tip.hasClass("fade")?s.one("bsTransitionEnd",g).emulateTransitionEnd(i.TRANSITION_DURATION):g()}},i.prototype.applyPlacement=function(e,i){var o=this.tip(),n=o[0].offsetWidth,s=o[0].offsetHeight,r=parseInt(o.css("margin-top"),10),l=parseInt(o.css("margin-left"),10);isNaN(r)&&(r=0),isNaN(l)&&(l=0),e.top+=r,e.left+=l,t.offset.setOffset(o[0],t.extend({using:function(t){o.css({top:Math.round(t.top),left:Math.round(t.left)})}},e),0),o.addClass("in");var a=o[0].offsetWidth,p=o[0].offsetHeight;"top"==i&&p!=s&&(e.top=e.top+s-p);var h=this.getViewportAdjustedDelta(i,e,a,p);h.left?e.left+=h.left:e.top+=h.top;var c=/top|bottom/.test(i),u=c?2*h.left-n+a:2*h.top-s+p,f=c?"offsetWidth":"offsetHeight";o.offset(e),this.replaceArrow(u,o[0][f],c)},i.prototype.replaceArrow=function(t,e,i){this.arrow().css(i?"left":"top",50*(1-t/e)+"%").css(i?"top":"left","")},i.prototype.setContent=function(){var t=this.tip(),e=this.getTitle();t.find(".tooltip-inner")[this.options.html?"html":"text"](e),t.removeClass("fade in top bottom left right")},i.prototype.hide=function(e){function o(){"in"!=n.hoverState&&s.detach(),n.$element&&n.$element.removeAttr("aria-describedby").trigger("hidden.bs."+n.type),e&&e()}var n=this,s=t(this.$tip),r=t.Event("hide.bs."+this.type);return this.$element.trigger(r),r.isDefaultPrevented()?void 0:(s.removeClass("in"),t.support.transition&&s.hasClass("fade")?s.one("bsTransitionEnd",o).emulateTransitionEnd(i.TRANSITION_DURATION):o(),this.hoverState=null,this)},i.prototype.fixTitle=function(){var t=this.$element;(t.attr("title")||"string"!=typeof t.attr("data-original-title"))&&t.attr("data-original-title",t.attr("title")||"").attr("title","")},i.prototype.hasContent=function(){return this.getTitle()},i.prototype.getPosition=function(e){e=e||this.$element;var i=e[0],o="BODY"==i.tagName,n=i.getBoundingClientRect();null==n.width&&(n=t.extend({},n,{width:n.right-n.left,height:n.bottom-n.top}));var s=window.SVGElement&&i instanceof window.SVGElement,r=o?{top:0,left:0}:s?null:e.offset(),l={scroll:o?document.documentElement.scrollTop||document.body.scrollTop:e.scrollTop()},a=o?{width:t(window).width(),height:t(window).height()}:null;return t.extend({},n,l,a,r)},i.prototype.getCalculatedOffset=function(t,e,i,o){return"bottom"==t?{top:e.top+e.height,left:e.left+e.width/2-i/2}:"top"==t?{top:e.top-o,left:e.left+e.width/2-i/2}:"left"==t?{top:e.top+e.height/2-o/2,left:e.left-i}:{top:e.top+e.height/2-o/2,left:e.left+e.width}},i.prototype.getViewportAdjustedDelta=function(t,e,i,o){var n={top:0,left:0};if(!this.$viewport)return n;var s=this.options.viewport&&this.options.viewport.padding||0,r=this.getPosition(this.$viewport);if(/right|left/.test(t)){var l=e.top-s-r.scroll,a=e.top+s-r.scroll+o;l<r.top?n.top=r.top-l:a>r.top+r.height&&(n.top=r.top+r.height-a)}else{var p=e.left-s,h=e.left+s+i;p<r.left?n.left=r.left-p:h>r.right&&(n.left=r.left+r.width-h)}return n},i.prototype.getTitle=function(){var t,e=this.$element,i=this.options;return t=e.attr("data-original-title")||("function"==typeof i.title?i.title.call(e[0]):i.title)},i.prototype.getUID=function(t){do t+=~~(1e6*Math.random());while(document.getElementById(t));return t},i.prototype.tip=function(){if(!this.$tip&&(this.$tip=t(this.options.template),1!=this.$tip.length))throw new Error(this.type+" `template` option must consist of exactly 1 top-level element!");return this.$tip},i.prototype.arrow=function(){return this.$arrow=this.$arrow||this.tip().find(".tooltip-arrow")},i.prototype.enable=function(){this.enabled=!0},i.prototype.disable=function(){this.enabled=!1},i.prototype.toggleEnabled=function(){this.enabled=!this.enabled},i.prototype.toggle=function(e){var i=this;e&&(i=t(e.currentTarget).data("bs."+this.type),i||(i=new this.constructor(e.currentTarget,this.getDelegateOptions()),t(e.currentTarget).data("bs."+this.type,i))),e?(i.inState.click=!i.inState.click,i.isInStateTrue()?i.enter(i):i.leave(i)):i.tip().hasClass("in")?i.leave(i):i.enter(i)},i.prototype.destroy=function(){var t=this;clearTimeout(this.timeout),this.hide(function(){t.$element.off("."+t.type).removeData("bs."+t.type),t.$tip&&t.$tip.detach(),t.$tip=null,t.$arrow=null,t.$viewport=null,t.$element=null})};var o=t.fn.tooltip;t.fn.tooltip=e,t.fn.tooltip.Constructor=i,t.fn.tooltip.noConflict=function(){return t.fn.tooltip=o,this}}(jQuery),$(".copy-text").tooltip({trigger:"click",placement:"top"});var clipboard=new Clipboard(".copy-text");clipboard.on("success",function(t){var e=$(t.trigger);setTooltip(e,"Copied"),hideTooltip(e)});
function Linkedin(){mywindow=window.open("https://www.linkedin.com/shareArticle?url="+location.href,"","width=640,height=540"),mywindow.moveTo(0,0)}$(document).ready(function(){$(".separator a").each(function(){var t=$(this),a=t.attr("href");t.attr("title",a.substring(a.lastIndexOf("/")+1,a.lastIndexOf(".")))}),$(".separator img").each(function(){var t=$(this),a=t.attr("src");t.attr("alt",a.substring(a.lastIndexOf("/")+1,a.lastIndexOf(".")))}),$(".avatar-image-container img").each(function(){var t=$(this),a=t.attr("src");t.attr("alt",a.substring(a.lastIndexOf("/")+1,a.lastIndexOf(".")))})});

jQuery.getScript('//cdn.firebase.com/js/client/2.3.2/firebase.js').done(function() {
$.each($("a[name]"),function(e,o){var t=$(o).parent().find("#postviews"),n=new Firebase("https://blogthuthuatwin10-e255b.firebaseio.com/pages/id/"+$(o).attr("name"));n.once("value",function(e){var a=e.val(),s=!1;null==a&&(a={},a.value=0,a.url=window.location.href,a.id=$(o).attr("name"),s=!0),t.text(a.value),a.value++,"/"!=window.location.pathname&&(s?n.set(a):n.child("value").set(a.value))})});});

$(document).ready(function() {
  jQuery('#ads_Code').appendTo(jQuery('a[name="more"]'));
  $('#recent-posts img').attr('src', function (i, src) {return src.replace('s72-c', 's1600')})
});

(function(d, s, id) {
  var js, fjs = d.getElementsByTagName(s)[0];
  if (d.getElementById(id)) return;
  js = d.createElement(s); js.id = id;
  js.src = 'https://connect.facebook.net/vi_VN/sdk.js#xfbml=1&version=v2.12&appId=434463203707259&autoLogAppEvents=1;
  fjs.parentNode.insertBefore(js, fjs);
  js.async=true;    
}(document, 'script', 'facebook-jssdk'));

 var uri = location.href;
  var getFacebookCount = function () {
  $.getJSON('https://graph.facebook.com/'+uri, function(data){
    var facebookShares = data.share.share_count;
    console.log(data);
    if (facebookShares) {
      $('.fbShare').append(facebookShares);
    } else {
   $('.fbShare').append(0);
    }
  });
};
getFacebookCount();

$('#sendBtn').click(function(){
  FB.ui({
    method: 'send',
    display: 'popup',
    mobile_iframe: true,
    link: location.href,
  }, function(response){});
});

$('#shareBtn').click(function(){
  FB.ui({
    method: 'share',
    display: 'popup',
    mobile_iframe: true,
    href: location.href,
  }, function(response){});
});

$('#feedBtn').click(function(){
  FB.ui({
    method: 'feed',
	display: 'popup',
    mobile_iframe: true,
    link: location.href,
  }, function(response){});
});

$(".printBtn").click(function() { 
  $('#taskbar,.header-right,#main_menu,#top-banner,.sidebar-wrapper,.breadcrumbs,.post-social,.knc-menu-nav,.related-post,#related-posts,.keywords,.social-sharing-widgets,.fb-comments,.ads_Gg,#comments,#PopularPosts1,#PopularPosts2,#HTML5,.footer-wrapper,#footer,.ads-right, .ads-left').css('display','none')
  $('body').css('background-color','#fff')
  $('#header-wrapper').css('background','unset').css('height','unset')
  $('.header-wrapper').css('border-bottom','2px solid #ccc')
  $('.main-wrapper').css('border','none')
  $('.box').css('float','none')
  $('.post-metaDescription,.related-post,.post-body').css('padding-left','0')
  $('.print').css('display','block')
  $('#HTML6,#HTML7').css('display','none')
});
//]]>
</script>
<script>
//<![CDATA[
//Related Posts
var randomRelatedIndex,showRelatedPost;!function(t,e,a){var l={widgetTitle:"",homePage:"/",numPosts:3,callBack:function(){}};for(var s in relatedPostConfig)l[s]="undefined"==relatedPostConfig[s]?l[s]:relatedPostConfig[s];var i=function(t){var l=e.createElement("script");l.type="text/javascript",l.src=t,a.appendChild(l)},r=function(t){var e,a,l=t.length;if(0===l)return!1;for(;--l;)e=Math.floor(Math.random()*(l+1)),a=t[l],t[l]=t[e],t[e]=a;return t},n="object"==typeof labelArray&&labelArray.length>0?"/-/"+r(labelArray)[0]:"";randomRelatedIndex=function(t){var e,a,s=t.feed.openSearch$totalResults.$t-l.numPosts,r=(e=1,a=s>0?s:1,Math.floor(Math.random()*(a-e+1))+e);i(l.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+n+"?alt=json-in-script&orderby=updated&start-index="+r+"&max-results="+l.numPosts+"&callback=showRelatedPost")},showRelatedPost=function(t){var e,a,s,i,n,m=document.getElementById(l.containerId),o=r(t.feed.entry),d=l.widgetStyle,h=l.widgetTitle+'<ul class="related-post-style-'+d+'">',c=l.newTabLink?' target="_blank"':"",p='<span style="display:block;clear:both;"></span>';if(m){for(var u=0;u<l.numPosts&&u!=o.length;u++){a=o[u].title.$t,s="auto"!==l.titleLength&&l.titleLength<a.length?a.substring(0,l.titleLength)+"&hellip;":a,i="media$thumbnail"in o[u]&&!1!==l.thumbnailSize?o[u].media$thumbnail.url.replace(/\/s[0-9]+(\-c)?/,"/s"+l.thumbnailSize+"-c"):l.noImage,n="summary"in o[u]&&l.summaryLength>0?o[u].summary.$t.replace(/<br ?\/?>/g," ").replace(/<.*?>/g,"").replace(/[<>]/g,"").substring(0,l.summaryLength)+"&hellip;":"";for(var g=0,b=o[u].link.length;g<b;g++)e="alternate"==o[u].link[g].rel?o[u].link[g].href:"#";h+=2==d?'<li><img alt="" class="related-post-item-thumbnail" src="'+i+'" width="'+l.thumbnailSize+'" height="'+l.thumbnailSize+'"><a class="related-post-item-title" title="'+a+'" href="'+e+'"'+c+">"+s+'</a><span class="related-post-item-summary"><span class="related-post-item-summary-text">'+n+'</span> <a href="'+e+'" class="related-post-item-more"'+c+">"+l.moreText+"</a></span>"+p+"</li>":3==d||4==d?'<li class="related-post-item" tabindex="0"><a class="related-post-item-title" href="'+e+'"'+c+'><img alt="" class="related-post-item-thumbnail" src="'+i+'" width="'+l.thumbnailSize+'" height="'+l.thumbnailSize+'"></a><div class="related-post-item-tooltip"><a class="related-post-item-title" title="'+a+'" href="'+e+'"'+c+">"+s+"</a></div>"+p+"</li>":5==d?'<li class="related-post-item" tabindex="0"><a class="related-post-item-wrapper" href="'+e+'" title="'+a+'"'+c+'><img alt="" class="related-post-item-thumbnail" src="'+i+'" width="'+l.thumbnailSize+'" height="'+l.thumbnailSize+'"><span class="related-post-item-tooltip">'+s+"</span></a>"+p+"</li>":6==d?'<li><a class="related-post-item-title" title="'+a+'" href="'+e+'"'+c+">"+s+'</a><div class="related-post-item-tooltip"><img alt="" class="related-post-item-thumbnail" src="'+i+'" width="'+l.thumbnailSize+'" height="'+l.thumbnailSize+'"><span class="related-post-item-summary"><span class="related-post-item-summary-text">'+n+"</span></span>"+p+"</div></li>":'<li><a title="'+a+'" href="'+e+'"'+c+">"+s+"</a></li>"}m.innerHTML=h+="</ul>"+p,l.callBack()}},i(l.homePage.replace(/\/$/,"")+"/feeds/posts/summary"+n+"?alt=json-in-script&orderby=updated&max-results=0&callback=randomRelatedIndex")}(window,document,document.getElementsByTagName("head")[0]);
//]]>
</script>

<!--<script src='https://apis.google.com/js/plusone.js' type='text/javascript'></script>-->


<script>



//<![CDATA[



//]]>
 


</script>

<script type="text/javascript" src="https://www.blogger.com/static/v1/widgets/3704019819-widgets.js"></script>
<script type='text/javascript'>
window['__wavt'] = 'AOuZoY7v6VjoknO_5WOz4bS5-w620O9OOA:1734321877337';_WidgetManager._Init('//www.blogger.com/rearrange?blogID\x3d4094428133207599602','//www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html','4094428133207599602');
_WidgetManager._SetDataContext([{'name': 'blog', 'data': {'blogId': '4094428133207599602', 'title': '\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh', 'url': 'https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html', 'canonicalUrl': 'https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html', 'homepageUrl': 'https://www.diachinhcongtrinh.com/', 'searchUrl': 'https://www.diachinhcongtrinh.com/search', 'canonicalHomepageUrl': 'https://www.diachinhcongtrinh.com/', 'blogspotFaviconUrl': 'https://www.diachinhcongtrinh.com/favicon.ico', 'bloggerUrl': 'https://www.blogger.com', 'hasCustomDomain': true, 'httpsEnabled': true, 'enabledCommentProfileImages': true, 'gPlusViewType': 'FILTERED_POSTMOD', 'adultContent': false, 'analyticsAccountNumber': 'UA-125429513-1', 'encoding': 'UTF-8', 'locale': 'en', 'localeUnderscoreDelimited': 'en', 'languageDirection': 'ltr', 'isPrivate': false, 'isMobile': false, 'isMobileRequest': false, 'mobileClass': '', 'isPrivateBlog': false, 'isDynamicViewsAvailable': true, 'feedLinks': '\x3clink rel\x3d\x22alternate\x22 type\x3d\x22application/atom+xml\x22 title\x3d\x22\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh - Atom\x22 href\x3d\x22https://www.diachinhcongtrinh.com/feeds/posts/default\x22 /\x3e\n\x3clink rel\x3d\x22alternate\x22 type\x3d\x22application/rss+xml\x22 title\x3d\x22\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh - RSS\x22 href\x3d\x22https://www.diachinhcongtrinh.com/feeds/posts/default?alt\x3drss\x22 /\x3e\n\x3clink rel\x3d\x22service.post\x22 type\x3d\x22application/atom+xml\x22 title\x3d\x22\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh - Atom\x22 href\x3d\x22https://www.blogger.com/feeds/4094428133207599602/posts/default\x22 /\x3e\n\n\x3clink rel\x3d\x22alternate\x22 type\x3d\x22application/atom+xml\x22 title\x3d\x22\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh - Atom\x22 href\x3d\x22https://www.diachinhcongtrinh.com/feeds/305187277557542461/comments/default\x22 /\x3e\n', 'meTag': '', 'adsenseClientId': 'ca-pub-7197786739659219', 'adsenseHostId': 'ca-host-pub-1556223355139109', 'adsenseHasAds': true, 'adsenseAutoAds': true, 'boqCommentIframeForm': true, 'loginRedirectParam': '', 'view': '', 'dynamicViewsCommentsSrc': '//www.blogblog.com/dynamicviews/4224c15c4e7c9321/js/comments.js', 'dynamicViewsScriptSrc': '//www.blogblog.com/dynamicviews/1cd72ec8369217df', 'plusOneApiSrc': 'https://apis.google.com/js/platform.js', 'disableGComments': true, 'interstitialAccepted': false, 'sharing': {'platforms': [{'name': 'Get link', 'key': 'link', 'shareMessage': 'Get link', 'target': ''}, {'name': 'Facebook', 'key': 'facebook', 'shareMessage': 'Share to Facebook', 'target': 'facebook'}, {'name': 'BlogThis!', 'key': 'blogThis', 'shareMessage': 'BlogThis!', 'target': 'blog'}, {'name': 'X', 'key': 'twitter', 'shareMessage': 'Share to X', 'target': 'twitter'}, {'name': 'Pinterest', 'key': 'pinterest', 'shareMessage': 'Share to Pinterest', 'target': 'pinterest'}, {'name': 'Email', 'key': 'email', 'shareMessage': 'Email', 'target': 'email'}], 'disableGooglePlus': true, 'googlePlusShareButtonWidth': 0, 'googlePlusBootstrap': '\x3cscript type\x3d\x22text/javascript\x22\x3ewindow.___gcfg \x3d {\x27lang\x27: \x27en\x27};\x3c/script\x3e'}, 'hasCustomJumpLinkMessage': false, 'jumpLinkMessage': 'Read more', 'pageType': 'item', 'postId': '305187277557542461', 'postImageThumbnailUrl': 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s72-c/2017-10-23_22-42-44.png', 'postImageUrl': 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png', 'pageName': 'T\u1ea3i v\u1ec1 g\xf3i ng\xf4n ng\u1eef v\xe0 h\u01b0\u1edbng d\u1eabn t\xedch h\u1ee3p v\xe0o b\u1ed9 c\xe0i Windows 10 version 1709', 'pageTitle': '\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh: T\u1ea3i v\u1ec1 g\xf3i ng\xf4n ng\u1eef v\xe0 h\u01b0\u1edbng d\u1eabn t\xedch h\u1ee3p v\xe0o b\u1ed9 c\xe0i Windows 10 version 1709', 'metaDescription': ''}}, {'name': 'features', 'data': {}}, {'name': 'messages', 'data': {'edit': 'Edit', 'linkCopiedToClipboard': 'Link copied to clipboard!', 'ok': 'Ok', 'postLink': 'Post Link'}}, {'name': 'template', 'data': {'name': 'custom', 'localizedName': 'Custom', 'isResponsive': true, 'isAlternateRendering': false, 'isCustom': true}}, {'name': 'view', 'data': {'classic': {'name': 'classic', 'url': '?view\x3dclassic'}, 'flipcard': {'name': 'flipcard', 'url': '?view\x3dflipcard'}, 'magazine': {'name': 'magazine', 'url': '?view\x3dmagazine'}, 'mosaic': {'name': 'mosaic', 'url': '?view\x3dmosaic'}, 'sidebar': {'name': 'sidebar', 'url': '?view\x3dsidebar'}, 'snapshot': {'name': 'snapshot', 'url': '?view\x3dsnapshot'}, 'timeslide': {'name': 'timeslide', 'url': '?view\x3dtimeslide'}, 'isMobile': false, 'title': 'T\u1ea3i v\u1ec1 g\xf3i ng\xf4n ng\u1eef v\xe0 h\u01b0\u1edbng d\u1eabn t\xedch h\u1ee3p v\xe0o b\u1ed9 c\xe0i Windows 10 version 1709', 'description': '\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh - Chia s\u1ebb v\xe0 h\u1ecdc h\u1ecfi ki\u1ebfn th\u1ee9c, ph\u1ea7n m\u1ec1m. MicroSation SE, MicroSation V8i, AutoCAD, Windows', 'featuredImage': 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png', 'url': 'https://www.diachinhcongtrinh.com/2017/10/tai-ve-goi-ngon-ngu-va-huong-dan-tich.html', 'type': 'item', 'isSingleItem': true, 'isMultipleItems': false, 'isError': false, 'isPage': false, 'isPost': true, 'isHomepage': false, 'isArchive': false, 'isLabelSearch': false, 'postId': 305187277557542461}}, {'name': 'widgets', 'data': [{'title': '\u0110\u1ecba Ch\xednh C\xf4ng Tr\xecnh (Header)', 'type': 'Header', 'sectionId': 'header', 'id': 'Header1'}, {'title': 'T\xecm ki\u1ebfm \u2193\u2193\u2193', 'type': 'HTML', 'sectionId': 'Ads-1', 'id': 'HTML1'}, {'title': '', 'type': 'HTML', 'sectionId': 'top-banner', 'id': 'HTML2'}, {'title': '', 'type': 'HTML', 'sectionId': 'lists1', 'id': 'HTML101'}, {'title': '', 'type': 'HTML', 'sectionId': 'lists5', 'id': 'HTML102'}, {'title': 'Blog Posts', 'type': 'Blog', 'sectionId': 'main', 'id': 'Blog1', 'posts': [{'id': '305187277557542461', 'title': 'T\u1ea3i v\u1ec1 g\xf3i ng\xf4n ng\u1eef v\xe0 h\u01b0\u1edbng d\u1eabn t\xedch h\u1ee3p v\xe0o b\u1ed9 c\xe0i Windows 10 version 1709', 'featuredImage': 'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBFt0j4XhtBywyzdQDnthK-vGHSHW5Ff0e0KqjWCfhJN2qMPnlEXYbQ8eVNaXEAmFCV5btA3VZyMjJnZm-UfnRyteRvUzibGW9gZJUBpEJd8JoY-zNmC1MkylXXomA5CUBNS5W0p-N1lkJ/s1600/2017-10-23_22-42-44.png', 'showInlineAds': false}], 'headerByline': {'regionName': 'header1', 'items': [{'name': 'share', 'label': ''}, {'name': 'author', 'label': 'B\u1edfi'}, {'name': 'timestamp', 'label': '-'}]}, 'footerBylines': [{'regionName': 'footer1', 'items': [{'name': 'icons', 'label': ''}]}, {'regionName': 'footer2', 'items': [{'name': 'labels', 'label': 'Labels:'}]}], 'allBylineItems': [{'name': 'share', 'label': ''}, {'name': 'author', 'label': 'B\u1edfi'}, {'name': 'timestamp', 'label': '-'}, {'name': 'icons', 'label': ''}, {'name': 'labels', 'label': 'Labels:'}]}, {'title': 'Advertisement', 'type': 'HTML', 'sectionId': 'main', 'id': 'HTML4'}, {'title': '', 'type': 'HTML', 'sectionId': 'main', 'id': 'HTML5'}, {'title': 'Ph\u1ed5 bi\u1ebfn trong tu\u1ea7n', 'type': 'PopularPosts', 'sectionId': 'main', 'id': 'PopularPosts1', 'posts': [{'title': 'B\u1ed9 c\xe0i MicroStation V8i full v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t', 'id': '4687517708895562532'}, {'title': 'Kh\u1eafc ph\u1ee5c l\u1ed7i Font ch\u1eef b\u1ea3n \u0111\u1ed3 tr\xean MicroSation V8i', 'id': '7399495273320176604'}, {'title': 'Ph\u1ea7n m\u1ec1m Microsation SE V7 Full t\xedch h\u1ee3p Famis TT25 m\u1edbi nh\u1ea5t v\xe0 IrasB, IrasC, GEOVEC', 'id': '590999135302149685'}, {'title': 'Download Global Mapper Full', 'id': '5037785344022470948'}, {'title': 'B\u1ed9 c\xe0i MicroSation V8i.SS4.08.11.09.832 v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t', 'id': '7753080846665579284'}, {'title': 'C\xe1c l\u1ed7i th\u01b0\u1eddng g\u1eb7p trong Microsation', 'id': '5893844958295589642'}, {'title': 'H\u01b0\u1edbng d\u1eabn chuy\u1ec3n b\u1ea3n v\u1ebd l\xean Google Earth b\u1eb1ng MicroSation V8i - \u0110\u01b0a b\u1ea3n v\u1ebd MicroSation, AutoCad, MapInfo l\xean Google Earth b\u1eb1ng ph\u1ea7n m\u1ec1m Global Mapper', 'id': '6554485838267755579'}, {'title': 'S\u1eeda l\u1ed7i font Famis v\xe0 TMV.Map tr\xean MicroSation nhanh ch\xf3ng \u0111\u01a1n gi\u1ea3n', 'id': '2989852112306832501'}]}, {'title': '', 'type': 'HTML', 'sectionId': 'main', 'id': 'HTML6'}, {'title': 'Tin T\u1ee9c', 'type': 'HTML', 'sectionId': 'main', 'id': 'HTML7'}, {'title': 'B\u1ea1n c\xf3 th\u1ec3 quan t\xe2m', 'type': 'PopularPosts', 'sectionId': 'main', 'id': 'PopularPosts2', 'posts': [{'title': 'B\u1ed9 c\xe0i MicroStation V8i full v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t', 'id': '4687517708895562532'}, {'title': 'Kh\u1eafc ph\u1ee5c l\u1ed7i Font ch\u1eef b\u1ea3n \u0111\u1ed3 tr\xean MicroSation V8i', 'id': '7399495273320176604'}, {'title': 'B\u1ed9 c\xe0i MicroSation V8i.SS4.08.11.09.832 v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t', 'id': '7753080846665579284'}, {'title': 'Download Global Mapper Full', 'id': '5037785344022470948'}, {'title': '  B\u1ed9 c\xe0i MicroSation V8.11_2004 v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t', 'id': '2595697184275525778'}, {'title': 'Ph\u1ea7n m\u1ec1m Microsation SE V7 Full t\xedch h\u1ee3p Famis TT25 m\u1edbi nh\u1ea5t v\xe0 IrasB, IrasC, GEOVEC', 'id': '590999135302149685'}, {'title': 'B\u1ed9 c\xe0i Famis TT 25 m\u1edbi nh\u1ea5t v\xe0 h\u01b0\u1edbng d\u1eabn c\xe0i \u0111\u1eb7t ph\u1ea7n m\u1ec1m Famis', 'id': '424558037854107388'}, {'title': 'C\xe1c l\u1ed7i th\u01b0\u1eddng g\u1eb7p trong Microsation', 'id': '5893844958295589642'}]}, {'title': '', 'type': 'Image', 'sectionId': 'Ads-3', 'id': 'Image3'}, {'title': 'MicroSation', 'type': 'HTML', 'sectionId': 'recent1', 'id': 'HTML103'}, {'title': '\u0110o \u0111\u1ea1c', 'type': 'HTML', 'sectionId': 'recent2', 'id': 'HTML104'}, {'title': '', 'type': 'Image', 'sectionId': 'Ads-4', 'id': 'Image4'}, {'title': 'MAPPING GIS', 'type': 'HTML', 'sectionId': 'magstyle4', 'id': 'HTML105'}, {'title': 'AutoCad', 'type': 'HTML', 'sectionId': 'recent3', 'id': 'HTML106'}, {'title': 'Windows', 'type': 'HTML', 'sectionId': 'magstyle44', 'id': 'HTML107'}, {'title': 'B\xecnh sai l\u01b0\u1edbi tr\u1eafc \u0111\u1ecba', 'type': 'HTML', 'sectionId': 'recent4', 'id': 'HTML108'}, {'title': 'Windows ISO', 'type': 'HTML', 'sectionId': 'magstyle1', 'id': 'HTML109'}, {'title': 'Ghost', 'type': 'HTML', 'sectionId': 'magstyle2', 'id': 'HTML110'}, {'title': '', 'type': 'HTML', 'sectionId': 'sidebar', 'id': 'HTML19'}, {'title': '', 'type': 'HTML', 'sectionId': 'sidebar', 'id': 'HTML21'}, {'title': '', 'type': 'HTML', 'sectionId': 'sidebar', 'id': 'HTML12'}, {'title': 'Bi\u1ec3u m\u1eabu li\xean h\u1ec7', 'type': 'ContactForm', 'sectionId': 'sidebar', 'id': 'ContactForm1'}, {'title': 'Li\xean K\u1ebft Link', 'type': 'LinkList', 'sectionId': 'footer1', 'id': 'LinkList1'}, {'title': 'Chuy\xean m\u1ee5c kh\xe1c', 'type': 'LinkList', 'sectionId': 'footer2', 'id': 'LinkList2'}, {'title': 'C\u1ed9ng \u0110\u1ed3ng', 'type': 'LinkList', 'sectionId': 'footer3', 'id': 'LinkList5'}, {'title': '', 'type': 'HTML', 'sectionId': 'footer4', 'id': 'HTML20'}]}]);
_WidgetManager._RegisterWidget('_HeaderView', new _WidgetInfo('Header1', 'header', document.getElementById('Header1'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML1', 'Ads-1', document.getElementById('HTML1'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML2', 'top-banner', document.getElementById('HTML2'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML101', 'lists1', document.getElementById('HTML101'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML102', 'lists5', document.getElementById('HTML102'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_BlogView', new _WidgetInfo('Blog1', 'main', document.getElementById('Blog1'), {'cmtInteractionsEnabled': false, 'lightboxEnabled': true, 'lightboxModuleUrl': 'https://www.blogger.com/static/v1/jsbin/2019811046-lbx.js', 'lightboxCssUrl': 'https://www.blogger.com/static/v1/v-css/1964470060-lightbox_bundle.css'}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML4', 'main', document.getElementById('HTML4'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML5', 'main', document.getElementById('HTML5'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_PopularPostsView', new _WidgetInfo('PopularPosts1', 'main', document.getElementById('PopularPosts1'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML6', 'main', document.getElementById('HTML6'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML7', 'main', document.getElementById('HTML7'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_PopularPostsView', new _WidgetInfo('PopularPosts2', 'main', document.getElementById('PopularPosts2'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_ImageView', new _WidgetInfo('Image3', 'Ads-3', document.getElementById('Image3'), {'resize': false}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML103', 'recent1', document.getElementById('HTML103'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML104', 'recent2', document.getElementById('HTML104'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_ImageView', new _WidgetInfo('Image4', 'Ads-4', document.getElementById('Image4'), {'resize': false}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML105', 'magstyle4', document.getElementById('HTML105'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML106', 'recent3', document.getElementById('HTML106'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML107', 'magstyle44', document.getElementById('HTML107'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML108', 'recent4', document.getElementById('HTML108'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML109', 'magstyle1', document.getElementById('HTML109'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML110', 'magstyle2', document.getElementById('HTML110'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML19', 'sidebar', document.getElementById('HTML19'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML21', 'sidebar', document.getElementById('HTML21'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML12', 'sidebar', document.getElementById('HTML12'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_ContactFormView', new _WidgetInfo('ContactForm1', 'sidebar', document.getElementById('ContactForm1'), {'contactFormMessageSendingMsg': 'Sending...', 'contactFormMessageSentMsg': 'Your message has been sent.', 'contactFormMessageNotSentMsg': 'Message could not be sent. Please try again later.', 'contactFormInvalidEmailMsg': 'A valid email address is required.', 'contactFormEmptyMessageMsg': 'Message field cannot be empty.', 'title': 'Bi\u1ec3u m\u1eabu li\xean h\u1ec7', 'blogId': '4094428133207599602', 'contactFormNameMsg': 'Name', 'contactFormEmailMsg': 'Email', 'contactFormMessageMsg': 'Message', 'contactFormSendMsg': 'Send', 'contactFormToken': 'AOuZoY7shJyJPKv-PdEI5uw1KFr_n2KnEg:1734321877338', 'submitUrl': 'https://www.blogger.com/contact-form.do'}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_LinkListView', new _WidgetInfo('LinkList1', 'footer1', document.getElementById('LinkList1'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_LinkListView', new _WidgetInfo('LinkList2', 'footer2', document.getElementById('LinkList2'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_LinkListView', new _WidgetInfo('LinkList5', 'footer3', document.getElementById('LinkList5'), {}, 'displayModeFull'));
_WidgetManager._RegisterWidget('_HTMLView', new _WidgetInfo('HTML20', 'footer4', document.getElementById('HTML20'), {}, 'displayModeFull'));
</script>
</body>
</html>
