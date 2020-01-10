# fts_furuhashi

<html lang="ja">
 <head>
  <meta charset="utf-8" />
	 

<style type="text/css">

  p {
color: #fffafa;
font-size: 1.5em;
 }
<!--
 .red {color:#ff0000;}
 .grey {color:#999999;}
 .snow {color:#fffafa;}
 .yellow {color:#ff0000; background:#ffff00;}
 .blue {color:#0000ff;}
 .white {color:#ffffff; blinking;}
 .waku {border:2px dotted #99cc66;
　　　　　　line-height: 200%;
　　　　　　padding: 10px;}
 -->
	
.date:before{content:"20181115";}
	
	
 #preview{
	position: relative;
	border: 3px solid #333;
	background: #444;
	padding: 5px;
	display: none;
	color: #FFF;
	text-align: center;
}

main {
background-color: rgba(255, 255, 255, 0.3);
}

section {
background-color: rgba(0, 225, 0, 0.5);
}

#wrap {background:none} /*PC用の背景はオフ*/
body::before {
  content:"";
  display:block;
  position:fixed;
  top:0;
  left:0;
  z-index:-1;
  width:100%;
  height:100vh;
  background:url(https://torokoid.github.io/fts_furuhashi/20181115_29.JPG) center/cover no-repeat; /*fixedをトル！*/
  -webkit-background-size:cover;/*Android4*/
  }
 
@media	screen and (min-width: 540px),
	screen and (orientation: landscape) {
   p.note { display: none; }
}
  
</style>

<link href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.7.1/css/lightbox.css" rel="stylesheet">
 
</head>
<body>
<p class="note">
  モバイル端末をお使いの場合は、画面を横向きにすると
  より見やすくご覧頂けます。
</p>
	
<h1><span class="blue"><strong>簡易、支払い＆精算計算</strong></span></h1>


        
<section>

<ul>
<li> <input type="button" id="btn1" value="精算計算  " onclick="btn1Click();" /> 　←　支払い＆精算計算、開始ボタン</li>
</ul>
    
<script>  
//ボタン１をクリックした時の処理
function btn1Click(){ 

var selects = prompt('参加人数を入力！');

var selectss = prompt('支払った人の人数を入力！');

var koukin = prompt('繰り越し金額を入力！');
    
var nama = [];
    for (var i=0; i<selectss; i++){
      nama[i] = prompt("支払った人の名前を入力");
    }   

var menu = [];    
    for (var i=0; i<selectss; i++){
      menu[i] = prompt(nama[i] + "さんの支払金額を入力");
    } 

document.write("各自の支払金額は<br>")
    for (var i=0; i<menu.length; i++){
      document.write(nama[i] + "さん：" + menu[i] + "円 <br>")
    }
    
//各自の会計額を計算
    
var kasann = [];
      kasann[0] = menu[0];
    for (var i=0; i<selectss-1; i++){
kasann[i+1] = Math.round (Number(kasann[i]) + Number(menu[i+1]));
      }
    
var kasan = Math.round (Number(kasann[i]) - Number(koukin))
      
//各自の分担分を計算

var buntan = Math.round (Number(kasan)/Number(selects));

//各自の割り勘分を計算

var wari = [];
    for (var i=0; i<selects; i++){
    wari[i] = Math.round (Number(menu[i]) - Number(buntan));
      }

var kasann = kasann[selectss-1]
    
document.write("<br>経費の総額：" + kasann + "円<br>")
      
document.write("公金補助額：" + koukin + "円<br>")

document.write("精算金額の総額：" + kasan + "円<br>")

document.write("参加人数は：" + selects + "人<br>")
      
document.write("一人当たりの分担：" + buntan + "円<br>")

document.write("<br>支払った人への払い戻し金額は<br>")
    for (var i=0; i<menu.length; i++){
      document.write(nama[i] + "さん：" + wari[i] + "円 <br>")
    }

document.write ("<br>以上、お帰りも気を付けて、次回も元気に再会～(^^)/"); 

document.write ("<br><br><a href="https://torokoid.github.io/fts_furuhashi/">2018/11/15,古橋さんご卒業記念パーティー → 戻る !</a> "); 

document.write ("<br><br><br><br>Copyright 2019/12/03 S.Hada @ HGT 1G1");

        document.bgColor = "#00ff80";
        document.fgColor = "blue";
    
}

    </script>
    
        </section>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>


<!--
<h1><span class="yellow"><marquee behavior="left">!!! 2020年1月24日(土)に元FTS伊藤さん、矢口さん、小林実さんのご卒業記念バーティー@魚盛 大宮店、が執り行われました !!!</marquee></span></h1>
<h2><span class="white">記念品目録</span></h2><br>
<h3><span class="white">for 伊藤さん</span></h3>
<a href="20200124_001.JPG" data-lightbox="abc"><img src="20200124_001.JPG" alt="サンプル画像" width="1800" /></a>
<h3><span class="white">for 矢口さん</span></h3>
<a href="20200124_002.JPG" data-lightbox="abc"><img src="20200124_002.JPG" alt="サンプル画像" width="1800" /></a>
<h3><span class="white">for 小林実さん</span></h3>
<a href="20200124_003.JPG" data-lightbox="abc"><img src="20200124_003.JPG" alt="サンプル画像" width="1800" /></a>
<h3><span class="white">実さん近況</span></h3>
<a href="20200124_004.JPG" data-lightbox="abc"><img src="20200124_004.JPG" alt="サンプル画像" width="1800" /></a>
<br><br><br><br><br>

-->


<h1><span class="yellow"><marquee behavior="alternate">!!! 2019年4月17日(水)に元FTS伊藤さんのご卒業記念お食事会が執り行われました !!!</marquee></span></h1>
<a href="20190417_002.jpg" data-lightbox="abc"><img src="20190417_002.jpg" alt="サンプル画像" width="1800" /></a>
<br><br><br><br><br>
<h1><span class="yellow"><marquee behavior="alternate">!!! 2018年11月15日(木)に元FTS古橋さんのご卒業記念パーティーが執り行われました !!!</marquee></span></h1>
<p align="right"><marquee direction="right" scrollamount="20" width="30%">(^_^)/~hada</marquee></p>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>
<div>
<h3><span class="white">↓ 画像はクリックで拡大します。スライドショーで閲覧できます。</span></h3>
<a href="20181115_02.JPG" data-lightbox="abc"><img src="20181115_02.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_03.JPG" data-lightbox="abc"><img src="20181115_03.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_04.JPG" data-lightbox="abc"><img src="20181115_04.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_05.JPG" data-lightbox="abc"><img src="20181115_05.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_06.JPG" data-lightbox="abc"><img src="20181115_06.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_07.JPG" data-lightbox="abc"><img src="20181115_07.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_08.JPG" data-lightbox="abc"><img src="20181115_08.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_09.JPG" data-lightbox="abc"><img src="20181115_09.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_10.JPG" data-lightbox="abc"><img src="20181115_10.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_11.JPG" data-lightbox="abc"><img src="20181115_11.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_12.JPG" data-lightbox="abc"><img src="20181115_12.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_13.JPG" data-lightbox="abc"><img src="20181115_13.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_14.JPG" data-lightbox="abc"><img src="20181115_14.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_15.JPG" data-lightbox="abc"><img src="20181115_15.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_16.JPG" data-lightbox="abc"><img src="20181115_16.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_17.JPG" data-lightbox="abc"><img src="20181115_17.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_18.JPG" data-lightbox="abc"><img src="20181115_18.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_19.JPG" data-lightbox="abc"><img src="20181115_19.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_20.JPG" data-lightbox="abc"><img src="20181115_20.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_21.JPG" data-lightbox="abc"><img src="20181115_21.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_22.JPG" data-lightbox="abc"><img src="20181115_22.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_23.JPG" data-lightbox="abc"><img src="20181115_23.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_24.JPG" data-lightbox="abc"><img src="20181115_24.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_25.JPG" data-lightbox="abc"><img src="20181115_25.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_26.JPG" data-lightbox="abc"><img src="20181115_26.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_27.JPG" data-lightbox="abc"><img src="20181115_27.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_28.JPG" data-lightbox="abc"><img src="20181115_28.JPG" alt="サンプル画像" width="360" /></a>
<a href="20181115_29.JPG" data-lightbox="abc"><img src="20181115_29.JPG" alt="サンプル画像" width="540" /></a>
<a href="20181115_30.JPG" data-lightbox="abc"><img src="20181115_30.JPG" alt="サンプル画像" width="90" /></a>
<a href="20181115_31.JPG" data-lightbox="abc"><img src="20181115_31.JPG" alt="サンプル画像" width="90" /></a>
<h4><span class="white">↑パノラマ・マジックで、少し歪んじゃった人が居たりしますが、ご愛敬〜〜(^_^)v。</span></h4><br>
<h4><span class="white">ここからは加藤さん撮影分。</span></h4><br>
<a href="20181115_32.JPG" data-lightbox="abc"><img src="20181115_32.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_33.JPG" data-lightbox="abc"><img src="20181115_33.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_34.JPG" data-lightbox="abc"><img src="20181115_34.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_35.JPG" data-lightbox="abc"><img src="20181115_35.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_36.JPG" data-lightbox="abc"><img src="20181115_36.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_37.JPG" data-lightbox="abc"><img src="20181115_37.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_38.JPG" data-lightbox="abc"><img src="20181115_38.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_39.JPG" data-lightbox="abc"><img src="20181115_39.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_40.JPG" data-lightbox="abc"><img src="20181115_40.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_41.JPG" data-lightbox="abc"><img src="20181115_41.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_42.JPG" data-lightbox="abc"><img src="20181115_42.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_43.JPG" data-lightbox="abc"><img src="20181115_43.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_44.JPG" data-lightbox="abc"><img src="20181115_44.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_45.JPG" data-lightbox="abc"><img src="20181115_45.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_46.JPG" data-lightbox="abc"><img src="20181115_46.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_47.JPG" data-lightbox="abc"><img src="20181115_47.JPG" alt="サンプル画像" width="100" /></a>

<h4><span class="white">ここからは雅代さん撮影分。</span></h4><br>
<a href="20181115_48.JPG" data-lightbox="abc"><img src="20181115_48.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_51.JPG" data-lightbox="abc"><img src="20181115_51.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_52.JPG" data-lightbox="abc"><img src="20181115_52.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_53.JPG" data-lightbox="abc"><img src="20181115_53.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_54.JPG" data-lightbox="abc"><img src="20181115_54.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_55.JPG" data-lightbox="abc"><img src="20181115_55.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_59.JPG" data-lightbox="abc"><img src="20181115_59.JPG" alt="サンプル画像" width="180" /></a>
<a href="20181115_60.JPG" data-lightbox="abc"><img src="20181115_60.JPG" alt="サンプル画像" width="180" /></a>
<br>
<a href="20181115_49.JPG" data-lightbox="abc"><img src="20181115_49.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_50.JPG" data-lightbox="abc"><img src="20181115_50.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_56.JPG" data-lightbox="abc"><img src="20181115_56.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_57.JPG" data-lightbox="abc"><img src="20181115_57.JPG" alt="サンプル画像" width="100" /></a>
<a href="20181115_58.JPG" data-lightbox="abc"><img src="20181115_58.JPG" alt="サンプル画像" width="100" /></a>

</div>

<h1>     <span class="blue"><strong>動画リンク集</strong></span></h1>
 <h3>
<p>横山さん、古橋さんのお言葉<br>
<iframe width="560" height="315" src="https://www.youtube.com/embed/W5K0uA5AadE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
<iframe width="560" height="315" src="https://www.youtube.com/embed/rfUiO9g_3ug" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</p></h3>

<br><br>
<main>
<span class="snow"><h3>・・・開催通知・・・</h3><br>
★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★<br>
From: Masayo Arai (荒井 雅代) <br>
Sent: Wednesday, October 31, 2018 11:17 AM<br>
To: Minoru Kobayashi (小林 実) <minoru_kobayashi@n.t.rd.honda.co.jp>; Yutaka Kamata (鎌田 豊) <Yutaka_Kamata@n.t.rd.honda.co.jp>; Hidehiko Anzai (安齊 秀彦) <hidehiko_anzai@n.t.rd.honda.co.jp>; Masashi Manita (間仁田 雅司) <masashi_manita@n.t.rd.honda.co.jp>; Yasuhiro Sakashita (坂下 泰広) <yasuhiro_sakashita@n.w.rd.honda.co.jp>; Yuji Saito (斉藤 祐司) <yuji_saito@n.w.rd.honda.co.jp>; '0nh75b05325615n@ezweb.ne.jp'; Toshio Yokoyama (横山 利夫) <Toshio_Yokoyama@n.t.rd.honda.co.jp>; Tadahiro Yaguchi (矢口 忠博) <tadahiro_yaguchi@n.w.rd.honda.co.jp>; JUN TOMIZAWA (冨沢 潤) <Jun_A_Tomizawa@hm.honda.co.jp>; Naomi Ito (伊東 尚美) <naomi_ito@n.w.rd.honda.co.jp>
Cc: Takero Shibukawa (澁川 岳郎) <takero_shibukawa@n.w.rd.honda.co.jp>; Shuichi Kato (加藤 秀一) <shuichi.kato@mail.a.rd.honda.co.jp>; Satoshi Hada (羽田 智) <satoshi_hada@n.t.rd.honda.co.jp><br>
Subject: 【場所決定】　FTS：古橋さんご卒業会<br>
 <br>
旧未来交通システム研究室の皆様<br>
（返信メールいただいた方のみのご連絡）<br>
 <br>
お世話様です。<br>
以下の日程で古橋さんご卒業会を開催いたします。<br>
改めて出席者の確認をしたいと思います。<br>
変更される方はご連絡ください<br>
期日：11月5日（月）まで<br>
 <br>
日時：11月15日（木）19:00～22:00<br>
場所：個室和食 傳～DEN～ 大宮店<br>
　　　埼玉県さいたま市大宮区仲町2-43-1 COMO大宮ビル3F<br>
　　　　https://r.gnavi.co.jp/d51a1y3d0000/menu7/<br>
内容：5500円コース　3時間飲み放題付<br>
予約名：渋川<br><br>
 
＜出席者＞　ご連絡いただいた順<br>
１．村田さん<br>
２．加藤さん<br>
３．(間仁田さん)<br>
４．斉藤さん<br>
５．横山さん<br>
６．小林さん<br>
７．安斉さん<br>
８．羽田さん<br>
９．(坂下さん)<br>
１０．渋川さん<br>
１１．矢口さん<br>
１２．(冨沢さん)<br>
１３．古橋さん（主賓）<br>
１４．荒井<br>
 <br>
コース料理を注文いたします。<br>
キャンセル料が発生することございます。<br>
ご了承ください。<br>
 <br>
 <br>
また、今回、記念品を用意しようと考えております。<br>
お勧めのお品ものございましたらご連絡ください。<br>
 <br>
 <br>
幹事長：渋川隊長<br>
幹事：加藤さん、羽田さん（HGT取りまとめ）、荒井<br>
 <br>
 <br>
★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★<br>
　<br>
荒井　雅代<br>
株式会社 本田技術研究所　R&DセンターＸ<br>
<br>
〒351-0188　埼玉県和光市本町8-1<br>
外線：080-4789-8853　内線：8705148<br>
FAX:048-462-5106<br>
E-mail:masayo_arai@n.w.rd.honda.co.jp<br>
<br>
★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★★</span><br>
</main>

<br><br><br><br><br><br>
<section>
<span class="snow"><h3>・・・古橋さん、ご挨拶メール。・・・</h3><br>


Seiichi Furuhashi (古橋 清一) globalhonda.onmicrosoft.com 経由<br>
12月19日(水) 15:35 (1 日前)<br>

To Toshio, Masayo, 自分, Hidehiko, Satoshi, Minoru, Shuichi, Tadahiro, Takero, Yuji, Yutaka, Seiichi<br><br>

旧FTSの皆さん<br><br>
 
先日の大宮での卒業式有り難うございました。<br>
久しぶりに皆様にお会いでき、楽しいひと時を過ごすことができました。<br><br>
 
本日をもちまして、31年間勤めてきたHONDAを定年退職します。<br>
31年間、楽しく、充実したHONDA人生でした。<br>
特に、多種多様なキャラクターが終結したFTSは大変印象深く残っています。<br><br>
 
飲んだ後の寝過ごしには充分気をつけて、<br>
健康に留意しこれからも頑張って下さい。皆様の活躍を祈っています。<br><br>
 
退職後の連絡先ですが、<br>
携帯：080-9200-1289<br>
携帯アドレス：seiichi_furuhashi@docomo.ne.jp<br>
となります。<br><br>
 
よろしくお願い致します。<br><br><br>

 
古橋<br>
</span>
</section>

<br><br><br><br><br><br>
<main>
<span class="snow"><h3>・・・開催翌週のメール会話が面白かったので記録しました。・・・</h3><br>
	
<br>
	
From: torokoid Mibu [mailto:torokoid@gmail.com] <br>
Sent: Wednesday, November 21, 2018 10:22 PM<br>
Subject: Re: 【ご連絡】　FTS：古橋さんご卒業会<br>

雅代さん撮影ぶんも追加しました。<br>

https://torokoid.github.io/fts_furuhashi/<br>

その他写真も随時受付中です〜😉😂<br>

羽田<br>

2018年11月20日(火) 21:52 torokoid Mibu <torokoid@gmail.com>:<br>

とりあえず、加藤さん撮影分の写真をHPに追加しました。<br>

追加写真も随時受付中〜😉<br>

https://torokoid.github.io/fts_furuhashi/<br>

羽田<br>

<br><br><br>

2018年11月20日(火) 10:18 Masayo Arai (荒井 雅代) <masayo_arai@n.w.rd.honda.co.jp>:<br>

■小林さん　<br>

那須塩原で3人いたとは・・・<br>

確かに宇都宮どまりの電車は安全ですね。<br>

お財布すられていないですか？本当に気をつけてくださいねーー<br>

■横山さん<br>

横山さんは紳士的なので（女性だけ？）<br>

小林さんを置き去りにするなんて信じられないと思っていました。<br>

ちゃんとお声がけしてくださったのですね。<br>

でも次は、小林さんをしっかり保護してあげてくださいねー。<br>

■古橋さん<br>

素直に私と武蔵野線経由で帰ればよかったのにーーー。<br>

そうしたら12時前には帰宅できましたよ。<br>

皆さんのメールを読みながら笑ってしまいました。<br>

先日の飲み会は、本当に楽しい飲み会でした！<br>

荒井雅代<br>

<br><br><br>

From: torokoid Mibu [mailto:torokoid@gmail.com] <br>
Sent: Monday, November 19, 2018 10:28 PM<br>
Subject: Re: 【ご連絡】　FTS：古橋さんご卒業会<br>

みなさま、お疲れ様です！<br>

羽田は新幹線の速度では危険なので、宇都宮止まりの快速で無事帰り着きました。<br>

宇都宮から岡本までは、奥様タクシーでした〜😂<br>

HPの方は、写真が集まってきたら、また更新して再配信しますのでお楽しみに。<br>

<br><br><br>

2018年11月19日(月) 20:55 Seiichi Furuhashi (古橋 清一) <seiichi_furuhashi@n.w.rd.honda.co.jp>:<br>

今日は実家のガスコンロが故障し、交換の為有休でした。 <br>

小林さんの寝過しで盛り上がってますが、 実は私も気付いたら武蔵小杉でした。時間は11時20分。次の上りは11時40分千葉行き。<br>

乗換案内で調べたら、東横線の武蔵小杉経由で家までたどり着けそうなので、10分歩いて東急武蔵小杉まで行ったら、今度は人身事故で自由が丘〜渋谷間が不通。<br>

でも乗るしかなくて、途中の停車駅、多分多摩川か田園調布で、反対ホームにたまたま目黒行きが来たのでそれに飛び乗って、何とか山手線経由で、西武池袋線の最終電

車に間に合いました。家にたどり着いたのは1時過ぎてましたが、ホットしました。<br>

武蔵小杉のタワーマンション群は、新幹線からいつも眺めてましたが、身近で初めて見ました。いい経験でした。<br>

ちなみに、大宮で乗った湘南新宿ライナーは国府津行きだったので、本当に途中で気付いて良かったです。<br>

皆様、飲んで電車で帰るときは、同方向の人と一緒に帰りましょう。一人のときは、空いていても、立っていれば寝過しません。<br>

古橋<br>

 iPhoneから送信<br>
 
 <br><br><br>

2018/11/19 19:18、Minoru Kobayashi (小林 実) <minoru_kobayashi@n.t.rd.honda.co.jp>のメール:<br>

横山さん<br>

帰りは終点が宇都宮のローカルを使うのが100%安全なので、次回はそうしたいと思います<br>

加藤さん<br>

N-VANですか？　何か食材でも仕入れにいくみたいでいいですね<br>

そろそろ不具合は収まっている頃だと思います<br>

小林<br>

<br><br><br>

From: Toshio Yokoyama (横山 利夫) <br>
Sent: Monday, November 19, 2018 7:07 PM<br>
Subject: RE: 【ご連絡】　FTS：古橋さんご卒業会<br>

小林さん<br>

横山＠本田技術研究所です。<br>
いつも色々とお世話になっております。<br>

確かにホームで遭遇して、私は小林さんに断わってからトイレの近くの車両に乗車しました。<br>

小林さんは、ホーム上で既に千鳥足だったので、今思えば近くに席に座っていればよかったかも<br>

しれません。次回は一緒に帰りましょう。<br>

ちなみに、横山は普通に宇都宮で降りました。<br>

 ------------------------------------------------------<br>

横山　利夫<br>

(株）本田技術研究所　四輪R&Dセンター<br>

統合制御開発室<br>

上席研究員(特任）<br>

〒321-3393<br>

栃木県芳賀郡芳賀町下高根沢4630番地<br>

Mobile: 090-8804-2188<br>

Mail: toshio_yokoyama@n.t.rd.honda.co.jp<br>

横山不在時には、<br>

吉葉 由美さん(028)677 3377(内）8767296<br>

Mail: yumi_yoshiba@n.t.rd.honda.co.jp<br>

まで連絡の程、宜しくお願い申し上げます。<br>

------------------------------------------------------<br>

<br><br><br>

From: Shuichi Kato (加藤 秀一) <br>
Sent: Monday, November 19, 2018 6:55 PM<br>
To: Minoru Kobayashi (小林 実) <br>
Subject: RE: 【ご連絡】　FTS：古橋さんご卒業会<br>
 
小林さん<br>
お疲れ様です。<br>
たいへんですね。普段からちゃんと寝てくださいね。<br>
N-VAN納車が今週末です。<br>
調子悪くなったら、小林さんに直接相談すれば良かったんでしたっけ？<br>
 
加藤（8724421）@HGAデザイン1BL<br>

<br><br><br>

From: Minoru Kobayashi (小林 実) <br>
Sent: Monday, November 19, 2018 6:47 PM<br>
Subject: RE: 【ご連絡】　FTS：古橋さんご卒業会 <br>

ホームで横山さんと会った気がしましたが、乗ったときは一人になっていて<br>

アラームセット前に眠り込んでしまいました<br>

ちなみに、那須塩原駅には３人の同じ境遇の人がいました<br>

<br><br><br>

From: Masayo Arai (荒井 雅代) <br>
Sent: Monday, November 19, 2018 6:37 PM<br>
Subject: RE: 【ご連絡】　FTS：古橋さんご卒業会<br>

え？<br>

誰も起こしてくれなかったのですか？？？？<br>

From: Minoru Kobayashi (小林 実) <br>
Sent: Monday, November 19, 2018 6:09 PM<br>
Subject: RE: 【ご連絡】　FTS：古橋さんご卒業会<br>

雅代さん<br>

会計と写真お疲れ様です<br>

私は、あの後、那須塩原～という声で目が覚めて、いたい目にあいました<br>

小林<br>

<br><br><br>

From: Masayo Arai (荒井 雅代) <br>
Sent: Monday, November 19, 2018 2:50 PM<br>
Subject: 【ご連絡】　FTS：古橋さんご卒業会 <br>

古橋さん<br>

お世話様です。<br>

15日の写真を羽田さんが以下の場所にまとめてくれましたので<br>

ご連絡します。<br>

後、ワインが届きましたので、お席に持って行きますね。<br>

荒井雅代<br>

＊＊＊＊＊<br>

<br><br><br>

みなさま<br>

昨晩は楽しい送別会をありがとうございました。<br>

手持ちの写真でHPを暫定構成してみました。<br>

https://torokoid.github.io/fts_furuhashi/<br>

お手元の写真を共有いただければ、HPに追加しますので、ご連絡下さい。<br>

羽田<br></span>
</main>
<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>	
	
	

<script src="https://code.jquery.com/jquery-1.12.4.min.js" type="text/javascript"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.7.1/js/lightbox.min.js" type="text/javascript"></script>


<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

<script type='text/javascript' src='https://torokoid.github.io/shiba/jquery.js?ver=1.12.4'></script>
<script src="https://torokoid.github.io/shiba/jquery.goup.min.js"></script>
<script src="https://torokoid.github.io/shiba/my.js"></script> 

<!-- フッタ -->
 <footer><span class="snow">
 Copyright 2018/11/16 S.Hada
	</span></footer>
