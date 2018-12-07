<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1-transitional.dtd">
<html lang="ja">
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<!--トラッキングコード-->
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.7/jquery.min.js"></script>
  <script>
    (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
    m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
    })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');
    ga('create', 'UA-88856706-1', 'auto');
    ga('send', 'pageview');
  </script>

  <link rel="" type="" href="">
  <title>九大謎解き企画Quest「Turns」解答ページ</title>
 </head>

 <body>
  <div id="wrap">
  </div>

  <div id="header">
   <h1><a href="Turnsロゴ.png"><img src="Turnsロゴ.png" height = 40rem width = 100rem></a></h1>
　 <h1><a href="Questロゴ.png"><img src="Questロゴ.png" height = 40rem width = 100rem></a></h1>
  </div>

<!--前説動画-->
  <p style="text-align:center;">
   <iframe width="720" height="480" src="1st動画.mp4" frameborder="0" allowfullscreen></iframe>
   
  </p>

<!--指示文-->
  <p style="text-align:center;">
   <img src="扉.png" width= 500rem heights = 1500rem>
  </p>

<!--解答フォーム-->
  <div id="wrap">
   <div class="kaitou">
    <div id="content">解答を入力して<br/>
     決定ボタンを押してください。</div>
    <form id="id_form" name="forml">
     <input id="id_textBox1" name="ans" type="text" placeholder="解答入力欄"/>
　　 <input type="button" value="決定する" onClick="test()" class="validate[required,equals[password1]]" id="kaitou-btn"/>
    </form>
   </div>

   <script type="text/javascript">
    jQuery(document).ready(function(){jQuery("#id_form").validationEngine();});
   </script>

   <script type="text/javascript">
<!--正答-->
    var answer1 ='あなたは大富豪';
    var answer2 ='あなたはだいふごう';
    var answer3 ='anatahadaihugou';
    var answer4 ='anatahadaihugo';
    var answer5 ='anatahadaifugou';
    var answer6 ='anatahadaifugo';
<!--入力の判定-->
    function test(){
             var ok="正解です。";
             var errors="解答欄が空白です。";
             var bodys='<body><div id="wrap">';
             var tagus='<b>'<font size="4">';
             var tagus2='</font></b>';
             ans=document.forms.id_textBox1.value;
                    if(ans==answer1 || ans==answer2 || ans==answer3 || ans==answer4 || ans==answer5 || ans== answer6){document.location.href="";}
             else if(ans==null){
                       alert(errors);}
             else{
                       showDialog();}
<!--ダイアログを表示する-->
    function showDialog(){
        var html = document.getElementByld("content").innerHTML;
        html = hyml + '<div id="dialog">'
                    + '<div id="dialog_back" style="height:" + getBrowserHeight() + 'px;"></div>`
                    + '<div id="dialog_body">'
                                    + '<span style="color:#000;font-size:15px;">'
                                    + 'もう一度考えてみよう。<br/><br/><br/>'
                                    + '</span>'
                                    + '<div style="text-align:center;">'
                                    + '<input type="button" onclick="closeDialog()" value="閉じる">'
                                    +'</div>
                    +'</div>'
                    +'</div>';
        document.getElementByld("content").innerHTML = html;
    }
<!--画面の大きさを取得する-->
    function getBrowserHeight(){
         if(window.innerHeight){
                return window.innerHeight;
         }
         else if ( document.documentElement &&
                   document.documentElement.clientHeight != 0 ) {
                   return document.documentElement.clientHeight;
         }
         else if ( document.body ) {
                   return document.body.clientHeight;
         }
    return 0;
    }
<!--ダイアログを閉じる-->
    function closeDialog() {
         var delNode = document.getElementById("dialog");
         delNode.parentNode.removeChild(delNode);
    }
   </script>
  </div>
 </body>
</html>
