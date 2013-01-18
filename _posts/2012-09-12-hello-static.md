---
layout: default
title: 權力回收：新站小記
tags:
- 電腦
- 心態
categories: 網誌
date: 2012-09-12 07:01
description: 本文包含了本站的構建史以及正在使用的程序的折騰情況。
---
新網站投入使用，這是個靜態站，不使用數據庫，代碼極簡單，但構建很複雜。也許有人不理解，好好的 Wordpress ，爲何忽然停用了？先照例聽聽我的鬼扯。  

曾幾何時， IT 界有一股 centralize 的趨勢，蘋果把硬件和軟件死死綁在一起，而微軟則將自己打造成一個從服務器到個人電腦到辦公套件再到娛樂休閒無所不包的強大體系。小小的開源 blog 程序，也紛紛做成 CMS 形式，不斷強化自身，變成超級怪物。這是因爲，當初電腦普及不久，軟件需要強大的團隊與雄厚的資金支持，否則難以成功。這就像中國走向統一是爲了治理黃河水患，沒有強大的政府力，誰也不能治理好黃河。而對於電腦水平普遍不高的個人而言，與其學會多款單一功能的軟件，不如學一款功能豐富如瑞士軍刀一般的強大軟件。  
但是，隨着時間發展，有自主意識的人已經體會到，那種強大、無所不包的商業軟件體系雖看似方便，但會形成一種令人作嘔的依賴性，有時這種依賴甚至是不可逆的（祇有蘋果公司卻能把這種專制包裝成叛逆，雖然明眼人一看就能明白這不過是營銷手段）。譬如說，你作爲一個普通的個人用戶，撰寫了大量的筆記，盡數使用 OneNote 來保存。有一天，你想用用 Linux 了，結果你的筆記就打不開了，祇好回到 Windows 下，繼續用你的 OneNote 。而且你最好祈禱 OneNote 的銷售量不要下滑，否則當他下滑到一定程度被 M$ 砍掉時，你會欲哭無淚，因爲下一代系統搞不好就不支持你的老掉牙 OneNote 了。想想罷，這該多可怕呢？（不過 OneNote 的情況還不錯，他的對手 EverNote 支持從 OneNote 導出。當然轉化效果各憑天命。）  
我們真的需要那麼多功能嗎？我們又真的能放心把自己的東西交給唯利是圖的資本家嗎？我們真的甘心被他們挾持嗎？我們爲什麼不去實現個人數據的 centralization ？這就對強大的體系形成一股推力，走向 decentralization 。於是開源社區崛起了。雖然開源軟件通常比較難上手，但他對於戒備心較強的人們具有莫名的吸引力。隨著初級編程知識的普及和各種易學編程語言的出現，原本安於傻瓜化軟件的人們越來越有條件實現自身 centralization 。  
此一趨向對於 IT 公司而言，無疑具有重大威脅。優秀的純單機軟件並非沒有生存空間，但空間一定會受到擠壓，商業公司面前無非兩種模式：一是繼續走蘋果式的捆綁硬件；二是新出現的與雲端服務結合。通過提供物品或附加服務來銷售軟件，是未來商業軟件的營銷模式。  
（以下文字各種情緒亂入，慎重閱讀。）

出於專業嗅覺，我對個人權力非常敏感，對我來說，依賴性越低才越好。我需要的是對數據的絕對控制，一旦不高興就能隨時打包走人。譬如做筆記，我試用了一陣子 Evernote ，非常不滿意其啟動速度和臃腫的數據結構（基於 sqllite ）。後轉 wiz ，就是看上他一個 note 一個文件，而且可以使用文本編輯器打開。但 wiz 的啟動速度同樣不爽，且文本編輯器雖能選擇，總不是原生支持，還曾弄丟少量文字。總而言之，我受夠了，就把筆記轉換成文本文件和少量 Excel ，丟進 Dropbox 。哪天不愛 Dropbox 了，把文件夾移出來就是。  
至於網站，我是文本編輯器控，對 Wordpress 那種必須在本地創建一個文本文件然後先登入再慢慢貼文章、打標籤、選分類的方式表示非常無奈。我也是刷新控，對預覽有比較多需求， Wordpress 預覽太慢，無法忍受。我還是修改控，頻繁修改卻還有數據庫潔癖， Wordpress 在修改文章的時候簡直弱爆了，不但會出緩存，大量佔用數據庫 ID ,而且改一次進一回後臺真不是人幹的事情。我總是在本地建立好文件（還要把後綴改成 html 以便不斷保存、刷新），改好後慢慢貼文章。但是人算不如天算，我經常就改一兩字或一兩句，專門爲此登入-找文章-進文章-修改（-進數據庫-找文章-刪緩存），邊際效益太低。我甚至寧可進 MySQL 改文章，也不要進 Wordpress 後臺，可見 Wordpress 對我來說用戶體驗多糟。這同時也表現了我對更底層的東西的一種期待，不過究其原因，還是上層建築無法滿足人民群眾我日益提高的需求。一言以蔽之，我就是不爽 Wordpress ，不爽 CMS 程序的後臺，不爽 MySQL ，不爽各種 database ，欲加之罪，其無辭乎。反正我負心薄幸，已經決定拋棄 Wordpress ，何愁找不到小三來見異思遷？  
上網逛了一圈，知道了 Git ，知道了 Jekyll ，知道了 Ruby ，祇是雖然 manuals totorials上各種簡單易用，我卻裝不好。但我堅信我是能夠調教好這類平臺的， TeX 都調教過（結果很慘，祇實現了基礎排版，而我需要的高級排版最後扔給那幫數學狂人無限鄙視的方正書版來處理），這種東西怎可能難得住我？不就是多讀文檔多嘗試嘛！重裝系統，裝了 railsinstaller 。有了這貨，很多事水到渠成，而我又看到了兩個靜態生成器選擇： Octopress 和 ruhoh 。鑒於 ruhoh 還處於開發初期，我先玩玩 Octopress ，畢竟這貨調用一下 Jekyll 就可以把 Wordpress 上的文章都導出了。可是命運似乎和我開了一個玩笑，無論我怎麼嘗試，在我導出文章後， Octopress 都不配合，死都不編譯。不編譯就不編譯唄，此處不留爺，自有留爺處，轉向 ruhoh 。在一段艱辛的排查之後，他終於 work 了。之前我把問題想得太複雜，其實這些都是很簡單的……  
說實話， ruhoh 非常難用。問題不在命令行操作，而在容錯。很多商業軟件的容錯能力非常高，而 ruhoh 卻很嚴格，少一個空格都罷工。這還不是結束， ruhoh 和 Jekyll 有些格式不兼容，比如文章日期、文檔命名方式等等。儘管我也有意趁此機會再刪掉一半以上的文章，逐個修改終究是非常辛苦的。還有這貨不支持 textile ，而僅有 markdown 或直接 html 。Textile 比 markdown 強了幾條街，但沒有也沒辦法不是，我這水平也不可能去動代碼核心。水平不夠，對某些事就不能太龜毛，本來打算把導航欄做成左讀，但是命令並沒有那沒簡單。還有他本身的標籤、分類都顯得非常簡陋，居然做不到一個標籤一個頁面，也沒有標籤雲。我也不大喜歡 Twitter Bootstrap ，對我來說，這貨字小色醜文章模版少，顯然不夠好。曾幾何時，在 Wordpress 下根本不要談什麼文章模版，不過現在自然要一番作爲，至少要把直排、橫排、橫排含代碼三者區分。好在我不是沒有主題設計的基礎，自己就開發過兩個 Wordpress 主題，所以一切修改都有所根據，相當於有自己的 bootstrap 。你現在看到的主題基本上是我一個晚上移植的，不過直排處理對我來說算是新鮮事，又多花了幾小時。  
ruhoh 好處當然很多。首先文章果然全都一篇一個文件的放到硬盤上了，修改很方便，備份可以說不用做，符合 centralization 標準。我喜歡預覽效果， ruhoh 祇要開了本地預覽，每次保存都能即時更新，裝一個瀏覽器自動刷新插件，再把文本編輯器的自動保存間隔設置得短一些，用起來跟 WYSIWYG 差不多了。或者你不要在本地做，自己寫好腳推文章，文章推到 GitHub 上再預覽也是不錯的。講到 GitHub ，也是一個令人愉快的經歷，速度、空間都很滿意，還不要錢。單個 repo 的空間是最好不大於 1GB ，對普通網站而言是足夠了。如果不夠，可以再開 repo 來做圖牀、音樂庫，或者用無限空間的 BitBucket 。當然，整體來講，功能肯定弱於 Wordpress ，但關鍵是我也用不了太多。  
嘮叨了半天都是我自己，那對於比較 general 的需求，靜態網站生成器又有什麼優勢呢？首先是速度。動態網站需要運算的內容較多，所以速度會被拖慢。你固然可以用偽靜態插件之類的東西，不過他從修改文章到靜態化完成不是不用時間，而且網站程序文件夾也會變得亂七八糟。不妨看看奧巴馬團隊的經驗。白宮網站是 Drupal 做的，他不需要盈利，所以用戶體驗不必做得多好。競選籌款站就不同了，這跟購物網站一樣，非常有必要做好體驗。於是他的團隊就用了 Jekyll ，訪問速度立刻獲得質的飛躍——當然了，一般小站不需要講太多用戶體驗，所謂用戶體驗，其實是做給自己的。不過自己賞心悅目也很好不是麼。  
大站靜態，小站爲神馬也要靜態？小站嘛，大家都不想多花錢。動態對服務器的要求比較高，免費空間少，高速免費空間可說不存在。但是對靜態站而言，還是存在的。現在米國網絡已實現社會主義初級階段了，有**大量** PaaS 可供使用，從全能的 <a href="http://sf.net" rel="external">Sourceforge</a>, <a href="https://openshift.redhat.com/app/" rel="external">Openshift</a>, <a href="http://www.heroku.com/" rel="external">Heruko</a>, <a href="http://www.cloudfoundry.com/" rel="external">CloudFoundry</a>, <a href="http://www.phpcloud.com/" rel="external">PhpCloud</a>, <a href="http://appfog.com/" rel="external">AppFog</a>, <a href="https://www.cloudcontrol.com" rel="external">CloudControl</a>, <a href="https://pagodabox.com/" rel="external">pagodabox</a>, <a href="https://www.dotcloud.com/" rel="external">dotCloud</a>, <a href="http://www.engineyard.com/products/orchestra" rel="external">Orchestra</a> 到比較單一的 <a href="https://appengine.google.com/" rel="external">Google App Engine</a>, <a href="https://github.com/" rel="external">GitHub</a>, <a href="https://bitbucket.org/" rel="external">BitBucket</a>  （免費 Git Hosting極多，詳見<a href="https://git.wiki.kernel.org/index.php/GitHosting" rel="external">此處</a>），對小站而言完全是免費的。在這大好的形式之下，或許小站不再需要收費空間了。不過上面提到的免費空間基本上支持 PHP 的速度都不是非常理想。我不清楚究竟是空間本身還是 PHP 網站本身，反正個人體驗是不如靜態。現在多數人用 Wordpress ，凡免費 PHP+MySQL 空間在中國都較容易抽風或牆掉。如果很文藝的用王國維三大境界來形容託管情況，大可這麼說：「昨夜西風凋碧樹，獨上新浪，寫盡天涯路」，「衣帶漸寬終不悔， WordPress 消得人憔悴」，「眾裏尋他千百度，回頭驀見， GitHub 正在，燈火闌珊處」。（新浪、天涯都提供託管博客服務。）  
Ruby 系的靜態網站生成器都與 Git 緊密結合。 Git 做的版本控制相信會帶給版本控各種無與倫比的享受。我甚至建議龜毛的作家也用 Git+BitBucket 來管理自己的作品。雖然我甚少回顧既有版本，不過偶爾看看還是不錯的。如果使用 Worpdress 等動態程序，就很難做版本控制了。即便保存一份草稿在本地，並且隔三差五 `Git commit` ，還是嫌不方便、不即時。  
總而言之， Git 系靜態網站生成器給我的感覺有幾點：首先， centralized ，一切掌握在自己手裏。其次，免費高速無廣告。第三，一次部署，終身無憂，備份、版本、發佈一體化，不需維護，站長唯一的任務就是把文章寫好、改好。  

一個 centralized 的國家需要強大的力量，而實現個人網站、數據、資料的 centralization 則需要強大的電腦水平——很遺憾我沒有。因此，我就做了半吊子 centralization ，其他未完成之部份，留待未來解決。  

**附一： ruhoh 用戶應備文檔及網頁**  
準備工作：圖省事就用 <a href="http://railsinstaller.org/" rel="external">RailsInstaller</a> 或 <a href="http://code.google.com/p/msysgit/downloads/list" rel="external">Git Portable</a> ，然後註冊並佈置好自己的 <a href="https://github.com/" rel="external">GitHub</a> 並部署。然後按照 <a href="http://ruhoh.com/" rel="external">ruhoh.com</a> 的貼心提示部署。如果覺得同步起來比較複雜，可以使用 <a href="https://code.google.com/p/tortoisegit/" rel="external">TortoiseGit</a> 。我的辦法是把上傳操作的幾條命令寫成一個 bat 文件，做好快捷方式，每次需要的時候點一下就行了。  
Git 教程： <a href="http://git-scm.com/book" rel="external">Pro Git</a> ——如果不用 GitHub 來存放，可以不看。  
Ruhoh 使用（務必）： <a href="http://ruhoh.com/usage/" rel="external">安裝</a>，<a href="http://ruhoh.com/usage/configure/" rel="external">個人信息</a>，<a href="http://ruhoh.com/usage/create/" rel="external">建文章</a>，<a href="http://ruhoh.com/usage/publish/" rel="external">發佈</a>，<a href="http://ruhoh.com/usage/templating/" rel="external">模塊</a>，<a href="http://ruhoh.com/usage/theming" rel="external">主題</a>，<a href="http://ruhoh.com/usage/widgets/" rel="external">部件</a>，<a href="http://ruhoh.com/usage/plugins/" rel="external">插件</a>，<a href="https://github.com/mojombo/jekyll/wiki/blog-migrations" rel="external">從他處搬家</a>。  
其他： <a href="http://daringfireball.net/projects/markdown/syntax" rel="external">Markdown</a> 或其<a href="http://markdown.tw/" rel="external">中文版</a> ，還可考慮 <a href="http://johnmacfarlane.net/pandoc/" rel="external">Pandoc</a> （需改代碼或再轉一次）。 ruhoh 模塊用 <a href="http://mustache.github.com/mustache.5.html" rel="external">Mustache</a> 標記，應讀。 <a href="http://jekyllbootstrap.com/" rel="external">Jekyll</a> 和 <a href="http://octopress.org/" rel="external">Octopress</a> 可以逛逛。最後，<a href="http://zoomquiet.org/res/scrapbook/ZqFLOSS/tree/item20070306123934-frameset.html" rel="external">這裏</a>有很多好東西。  
以上就是我在大量瀏覽之後總結出來的少量網站，雖然好像也不算很少，不過如果想完全掌握好 ruhoh ，看這些當然遠遠不夠了。比如要製作主題，那麼整個默認主題當然要細究一番。這也是一個非常好的例子，間接證明了開源程序的坑爹性。不過，雖然有部分莫名其妙的所謂技術人士指出， ruhoh 等物有這些那些 prerequisites ，是程序猿的東西，還揚言不懂 console 就不行。但從我的經歷看，其實祇有兩樣：一是較多的網頁製作經驗，即 html + CSS 。二是四級以上英語水平（閱讀能力跟英語國家小學三年級差不多吧），以便讀文檔、搜索。如果你再問我還有什麼，那我就說， 105 以上的智商。但智商 105 以下的，我還真沒聽說誰既懂 html ，又英語過四級，又能讀以中文撰寫的本文，且看了上面那一大篇遠比文藝青年作品難懂的文字，還能耐著性子讀到這裏。  
好吧， ruhoh 上手後也沒什麼，即使是重裝系統，裝上 railsinstaller ，到 GitHub 網站上加一下新的 ssh key ，然後 `gem install ruhoh` （不打算本地編譯的話這一步可以省略），即可。如果遺失本地的備份（以用戶名爲 821 爲例）， `git clone git@github.com:821/821.ruhoh.com.git 821` ，一切都回來了。發佈文章也簡單，改好後 `git add .` `git commit -m 'yymmdd'` `git remote set-url origin git@github.com:821/821.ruhoh.com.git` 再 `git push origin master` 搞定。如果密鑰不見了，那就生成一個唄。雖然肯定不像某些白癡程序那麼方便，但也不很麻煩。網站更新後大約一分鐘就能看到了，還是挺快的。  
我的上傳 bat ：
{% highlight bash %}cd ruhoh
call git add .
call git add -A
call git commit -m "%date:~0,10%"
call git push origin master
{% endhighlight %}
  
  
**附二：對比 Wordpress 與 ruhoh**  
二者都有的優點：  
開源、免費。  
有時一方的優點即是對方的缺點：
Wordpress: 學習曲線平緩、內建功能多（反對者也可以認爲功能過多）、插件多、中英文檔都豐富、不需本地部署。  
ruhoh: 對空間的要求低、備份和搬家更輕鬆（文章本來就在電腦裏，而更新和搬家的區別僅僅是命令有幾個字母不同）、速度快、修改方便、支持 Markdown 等簡潔的標記語言、 GitHub 社區裏大量知名程序猿、不存在安全漏洞、自由度更高、方便版本控制。  
一方令人難以忍受，但對方也有些無奈的缺點：  
Wordpress: 特殊的專用 PHP 命令讓資深程序猿反而還要學他、留言也佔用數據庫條目導致臃腫化。  
ruhoh: 萬惡的 Mustache 導致模版**有時**非常難搞、留言需要用閉源服務管理且切換域名時需要重新導入。  

**附三：我的網站旅程（舊文，有增刪）**  
我老人家開始自己的個人網站旅程，乃是非常曲折而白痴的。這段旅程從我老人家極度不滿 fb 的網誌開始（這口吻是看西方理論作品的後遺症），但在 fb 以前，我老人家也用過其他的網誌。大家就順著我老人家的旅程來看一看吧。  

<span style="color: #ff0000;">起家： QQ 空間</span>  
OMG ，他還沒倒閉？真是奇蹟！這是我老人家對 QQ 空間的評價。那時高中剛畢業，註冊了 QQ ，爲了方便好友「觀賞」，就在上面寫。但是， QQ 空間即使在中國使用，速度都非常慢，而且換皮膚之類都很煩。居然還有一堆收費項目，我老人家當時就很好奇：花錢在 QQ 空間上的人腦子都進水了嗎？  

<span style="color: #ff0000;">真正開始寫網誌： MSN space</span>  
可憐的我老人家開始了洋插隊生活。插隊大半年， MSN 越用越爽，乾脆在上面寫起網誌來。那時一直有寫日記的習慣，所以網誌上基本是日記。後來覺得寫日記不如寫網誌有效率，就用網誌了。湛也說，在外讀書，無法背負那麼多紙張上路。  
可是用了一段時間，就發現他有些短路。雖然這裏很方便 MSN 好友觀看，但是沒有 MSN 的人無法留言。而 MSN 在中國人氣遠不如 QQ ，實在不大好。更何況標籤功能在很多網誌都出現了， MSN 就是沒有。  
不過我還是忍了三年。  

<span style="color: #ff0000;">淺嘗輒止：校內網</span>  
那時聽說中國有了個網站新秀，叫校內網。我老人家磨蹭了一年多才去註冊了一個號。好友不過二十多人。那時我老人家正在寫 msn 網誌，僅有極少文字出現於斯，所以非常不重要。  

<span style="color: #ff0000;">非死不可</span>  
fb 的網誌真是垃圾到家！！！簡直就是一個簡陋的留言板。  
我老人家在用了一年校內後得知，其實校內是 fb 的山寨，二者介面都很像。區別是 fb 有豐富的語言介面，我老人家可以使用繁體中文版；還有 fb 因爲比較好用而被 GFWed 。在 Yizhen 小朋友的推薦之下，我老人家決定試試，上面一大半都是中文系的朋友。  
我老人家隨手寫了幾篇網誌，就發現 fb 的網誌系統爛到極點，所以開始了新的選擇。  

<span style="color: #ff0000;">一篇都沒寫： blogspot</span>  
我很喜歡衣老師的網誌，這個網誌就放在 blogspot 上。在氣憤 fb 之餘，上 blogspot 玩了玩。  
我老人家很快發現， blogspot 有個有趣的功能：匯入。於是我辛辛苦苦把 MSN 的 500 多篇廢話用網路上教的方法下載下來（中間斷了 N 次，又手動續了 N 次），才好不容易把這 1.5MB 的 xml 檔弄到手－－結果發現，居然無法匯入。真是欺騙感情！！一怒之下，搬家。  

<span style="color: #ff0000;">過渡： Wordpress.com</span>  
這個網誌在介面上是高度自由了，但是上傳歌曲之類的不甚方便。  

<span style="color: #ff0000;">其他選擇</span>  
我老人家考慮過很多選擇。譬如個人認爲台灣最好的 xuite ，或者人氣很高的無名小站，都值得考慮。不過，兩個網誌的介面無法高度自由化（也就是變成像現在你看到的那麼簡陋），我老人家考慮之後都放棄了。中國那些簡化字的託管，當然不在考慮之列。不光是因爲簡化字，還有河蟹。像我老人家這種草泥馬飼養員怎麼可能跟河蟹共存？而且我經常替各種異類觀點講話，就算不被河蟹，也要被砲轟。所以，最好能有一個無法百度到的網誌。  
還有就是，我對導出功能非常強調，如果無法導出，說明該託管是流氓，用數據來綁架客戶。中國絕大多數託管都是流氓，米國也有一個大流氓叫 MSN Space ，至於 Facebook 這些，我也視爲流氓，因爲我找不到導出。  

<span style="color: #ff0000;">Wordpress.org</span>  
記不起什麼原因，我搜索到了<a href="http://blog.epic2016.com/" rel="external">太平盛世</a>，一個懂點 html 的文科教員的個人站。他的網站吸引我的當然不是格式，而是內容本身，祇不過同時覺得他的站挺舒服，沒有各種刺眼的、令人反感的元素。於是嘗試了 Wordpress 。嘛，所以說我的個人網站經歷竟然始於一位文科女士的網站，而不是任何一隻程序猿、碼農。這同時說明，網站的內容比形式要重要。  
Wordpress 很不錯，且不說沒有廣告，單是那自由度，就讓你很想試試。主題也不難編輯，畢竟有個模版再編輯主題，可以忽略掉很多 PHP 或 Wordpress PHP 知識。  

<span style="color: #ff0000;">從使用到製作</span>  
以上歷程可以視爲小白史，不過人總是要進步的。  
像我這樣個性過於鮮明，想法過於詭異的人，當然期待更高的自由度，更多的修改空間。遇到一個開源的系統，自然會對他動手動腳。我把主題大刀闊斧的刪掉了許多，又把很多插件融入主題，再搜索了一些我覺得比較有趣的功能，終於自行實現了代碼高亮以外所有需要的東西（順帶學了一丁點 PHP ）。至此，我的 Wordpress 折騰全部結束，對我而言，我的網站已經無限近乎 Wordpress 完美體了。  

<span style="color: #ff0000;">偉大的歷程</span>  
在鼓搗個人網站之前，我完全沒有修讀過任何一門電腦方面的課程，一切電腦知識都是娛樂性的。但開始做站之後，似乎開啟了一扇小門，學習了各種知識，還上網找了一些名校的電腦課來聽聽。雖然完全沒有做出任何一件像樣的作品，卻漸漸瞭解了程序猿的世界。  
這些經歷在實質上幾乎沒有幫助，但當我面對一些對初級用戶比較不友好的東西時，會比原先更從容，也更習慣 IT 業界，特別是開源社區的運作模式。這就是一番鼓搗背後的意義。