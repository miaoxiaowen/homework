<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>网传管网</title>
<link rel="stylesheet" type="text/css" href="assets/style.css" />
<link rel="stylesheet" type="text/css" href="assets/swiper-3.4.0.min.css" />
</head>

<body>
<div class="content">
	<div class="header">
        <img src="img/logo.png">
        <div class="quickLink">
            <a href="#">教师进入</a>
            <a href="#">教师进入</a>
            <a href="#">教师进入</a>
        </div>
    </div>
    <div class="nav">
        <ul>
            <li><a href="#">首页</a></li>
            <li><a href="#">学院概况</a></li>
            <li><a href="#">专业设置</a></li>
            <li><a href="#">教育教学</a></li>
            <li><a href="#">科学研究</a></li>
            <li><a href="#">教师发展</a></li>
            <li><a href="#">党建思政</a></li>
            <li><a href="#">作品展示</a></li>

        </ul>
    </div>
    <!--swipe的内容区域-->
    <div class="swiper-container" id="bannerSwiper">
        <div class="swiper-wrapper">
            <div class="banner swiper-slide"></div>
            <div class="swiper-slide">Slide 2</div>
            <div class="swiper-slide">Slide 3</div>
        </div>
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
    </div>
    <!--swipe end-->
    <!--页面的主体部分-->
    <div class="container">
        <div class="row">
            <!--id 唯一的 class 可以重复使用的-->
            <div class="cols" id="cols1-1">
                <div class="swiper-container" id="newsSwiper">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide"><img src="img/01.jpg"></div>
                        <div class="swiper-slide"><img src="img/02.jpg"></div>
                        <div class="swiper-slide"><img src="img/03.jpg"></div>
                    </div>
                    <div class="swiper-pagination"></div>
                    <div class="newsTitle">标题</div>
                </div>
            </div>
            <div class="cols" id="cols1-2">
                <ul>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                    <li>
                        <span class="channel">[栏目]</span><a href="#">&nbsp;&nbsp;&nbsp;&nbsp;标题标题标题标题标题</a><span class="datetime">2017/3/31</span>
                    </li>
                </ul>
                  </div>
            <div class="cols" id="cols1-3">
                <span class="title">学院概况</span>
                <p>
                    网络传播学院是中国互联网新闻中心与浙江越秀外国语学院合办的中国互联网人才培养的重要基地，其培养目标是：为中国互联网行业培养高素质、高层次的互联网媒体新闻、经营、技术和管理人才。 学院现有编辑出版学、传播学、新闻学、网络与新媒体和数字媒体艺术五个本科专业。
                </p>
            </div>
        </div>
        <div class="row"></div>
        <div class="row"></div>
    </div>

</div>
</body>
<!--脚本的标签 js文件 依赖的文件一定要写在最上面-->
<script src="assets/jquery-3.1.1.min.js"></script>
<script src="assets/swiper.jquery.min.js"></script>
<script>
   <!--var 定义一个变量, new 初始化了一个控件-->
    var mySilde = new Swiper ('#bannerSwiper', {
        loop: true,
        nextButton: '.swiper-button-next',
        prevButton: '.swiper-button-prev',
    })
//    获取浏览器的视口的宽度
    var width = $(document).width();
    var height = width *300 / 2000;
    $('#bannerSwiper').css('height',height + 'px');

   var newsSwiper = new Swiper ('#newsSwiper', {
       autoplay: 4000,//可选选项，自动滑动
       pagination : '.swiper-pagination',
       paginationType : 'progress',
       effect : 'fade'
   })
    //设置长和高
        var newsSwiper =  $('#newsSwiper .swiper-wrapper').children();
       newsSwiper.each(function () {
          $(this).children().attr({
                   "width":"300",
                   "height":"220"
           });
       })



</script>
</html>
