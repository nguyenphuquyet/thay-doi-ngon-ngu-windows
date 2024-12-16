
<div class='post-title'><h1>Tải về gói ngôn ngữ và hướng dẫn tích hợp vào bộ cài Windows 10 version 1709</h1></div>
<div class='post-meta'>

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
