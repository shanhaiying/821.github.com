---
layout: indexed
title: TeX 傳統版式寫作的曲折道路
tags:
- 電腦
date: '2013/03/11'
---
（文章動筆於 2013/02/25 ，初稿完成於 2013/03/11 ，修訂於 2014/11/24 ——主要是 TeX 開發活躍，文章的維護性更新很有必要；同時爲了維持文章篇幅，做了一些減法。）

本文的主題是用 TeX 進行傳統版式寫作。分析一下句子成分，首先是「寫作」而不是單純排版，其次所寫內容排出來是傳統版式的。單純排版， Adobe InDesign 更簡單，不過其性能不適合寫作。單純的寫作同時稍微排版一下，嘛，我不就在用 textile 寫本文嗎？但這種排版是比較簡單的，很多地方衹能將就。所以說，這裏討論的內容極端特殊，有人會覺得有點變態的。
TeX 的功能就是寫作的同時顧及排版，故而 TeX 用戶羣在寫作能力上遠超其他軟件用戶羣，網上各種文檔還是比較豐富的，衹是由於 TeX 更新較快且體系龐雜，纔會讓人誤以爲這貨很難駕馭。本文書寫重點是網絡上較少談到，或較少以我能正常閱讀的文字爲載體討論的。

## 缺點
個人認爲，談論一款軟件不應從優點說起，而是缺點。受衆先瞭解缺點，就能從而及時放棄，不要浪費時間去學習。

#### 學習曲線
像 Word 那樣，一個半文盲民工打開軟件，打一段話，點點鼠標，就能排出點什麼東西，有時看看還挺複雜。這是商業軟件的特點，一開始給你一點美好憧憬，到你習慣了、捨不得丟開了，纔知道有多難。
TeX 就不能這樣，什麼文檔也不讀的話，最簡單的東西都不能排。

#### 麻煩
TeX 囉嗦程度略小於 html 。但事實上我更常用 html ，而非 TeX 。爲什麼？
首先， html 不存在編譯問題，開頭、結尾聲明不錯就行。 TeX 則涉及命令定義和宏包等問題，較複雜，失敗率高，而且編譯環境安裝起來有點煩人。
其次，雖然 html 和 TeX 都有點囉嗦，但 html 有簡化的 markdown 和 textile ， TeX 沒有。

#### 一切皆 beta
對於很多商業軟件，比如同類型的方正書版，或 Adobe InDesign ，再或毫無干系但常有人拿來對比的 Office ，他們都有個特點：從某個版本起，就有一種較穩定的感覺了。方正書版，現在很多人還在用上世紀的版本；而 Office ，使用 2003 和 2007 的非常多； Adobe InDesign 用戶也往往不那麼急着更新。爲什麼？穩定了，就不追求升級了。
這在 TeX 世界完全不可行。就說中文，十年前還在 CCT ，後來 CJK ，再後來 pTeX 和 XeTeX ，現在是 LuaTeX-ja 和 XeTeX 平分秋色。所學知識兩三年要大更新一次，衹有最基礎的 Plain TeX 知識可以五十年不變。就像很多母程序猿的抱怨一樣：生完小猿回來，什麼都不會了。公猿如果休假長一點也會這樣。
特別是中文直排這種小衆需求，現在還有很多問題，用戶自己也會期待更新。（不過我比較煩各種 unstable 版本，還是喜歡等 TeX Live 出高大全。）

#### 永遠有那麼一點點區別
TeX 可以排得很美，也可以比 Word 還醜。美醜間是一些初學者不容易掌握的細微設置和環境差異。
在網上看到別人一個極美觀的排版時，不要過度雞凍，因爲我們排不出的可能性是 99% ——除非你能把對方的環境和設置完美 copy 到自己電腦裏，但有時一個宏包的升級，一個發行版的變更，就能輕易的將模板毀容（除非他強到完全用 Plain TeX 來寫，但代碼的可讀性直線下降，能借來用的肯定不是一般人）。有點差別還算好情況了，更糟的是編譯失敗……
這個情況隨着 TeX 及各種發行版的進步有所緩解，不過仍然常有陷阱。而且很奇怪的是，網上很多人發模板，但很少人在模板的註釋裏提到編譯環境。更有喪心病狂者，模板裏使用某個 Google 不到的生僻宏包，還不附上下載地址……

#### 坑爹的環境，龐雜的體系
TeX 是開源軟件體系。開源軟件已經夠坑爹了，而「開源軟件體系」有多坑爹，可想而知。
一個可運行的 TeX 環境，文件數量一般都上萬（ TeX Live 套裝早已突破十萬），體積當然也不小。對於單文件綠色版的用戶來說，無疑是痛苦的。
都是 TeX 的子孫，引擎一換，很多宏包無法互通，自己寫命令的時候也要很小心。如果要從 LaTeX 跳槽 ConTeXt ，會有一段時間感到無所適從。
更該死的是，很多需要的文檔並不那麼好找，或者找到了卻發現不是英文的，再或者根本沒文檔（這種情況常見於跑單幫作者開發的包）。

#### 中文、中式排版資源匱乏
中國人缺乏鑽研精神，對美的要求也不高，所以 TeX 的中文資源相對較少。
由於 TeX 是針對西方語言編寫的，對傳統中式排版和中文並非先天支持，這本來需要一個強大的本地社區，偏偏這社區很弱小，大家衹好努力鍛鍊個人技能了。

## 爲了這些就別看 TeX 了

#### 幾個破式子或化學結構式
Word 2007 開始支持 TeX 式的公式輸入。化學用 ChemDraw 。
TeX 排公式的視覺質量比 Word 要好，那是毋庸置疑的，不過很多人的目標衹是「排出來」而不是「排得好看」罷？

#### 無規律複雜文檔
如果你要排板報、書籍封面等花式較多且規律性比較弱，而且也就幾頁的東西，用 InDesign, PhotoShop, Microsoft Visio, 方正飛騰即可，不要到 TeX 下折騰。事倍功半。

#### 其他軟件能完美實現並高效便捷修改的
比如中文直排，如果你不像我一樣需要一大堆複雜的規則化板式，如眉批、夾批、夾注、書耳之類，而僅僅是要一個最簡單的直排，何必 TeX 呢。 TeX 的學習成本是最高的。

## 用戶條件
TeX 主要是給研究人員用的，本文討論的又是複雜的中/日式排版（我要實現的東西更像日式排版），所以對用戶也是有點條件的。
一、無障礙閱讀英文科技短文（必須）
二、耐心（必須）
三、對編碼、字體有基本瞭解（要弄字體則必須）
四、開源軟件使用經驗（幾乎必須，這是一種習慣）
五、習慣邊構思邊打字（非必須，但如果非要先寫手稿纔上機，還眞比較痛苦，除非打字像 Knuth 那麼快）
六、初中平面幾何無不及格記錄（非必須，但如想弄點複雜的東西，估計夠嗆）
七、腦袋從未被驢踢或門夾（必須，比如有人堅持認爲在 InDesign 裏一個個加樣式比用文本編輯器批量替換容易，我還眞沒辦法了）
順帶說一下，雖然我不認爲 TeX 太難，不過臺灣有個叫侯捷的程序猿，因覺 TeX 難，就用 Word ，還出了一本叫「 Word 排版藝術」的書（這本書產生的年代 TeX 排中文確實有點煩，但也不至於那麼誇張）。

## 優點
如果還沒嚇退讀者，這位讀者必定心靈堅強，對美有自己的追求，九成以上可能性是研究生/博士生/研究機構人員/獨立研究人員/有計畫從事研究的大學生/出版業工作者/電腦狂人，這些人多數都符合條件，可以瞭解一下 TeX 的優點並考慮使用。

### 善於處理巨著
我們都知道 Word 處理長篇文檔時多麼不可愛。 TeX 的文件都是文本文檔，而且你可以做成一章一個文件，然後整體一起編譯。
不過換句話說，排一兩頁臨時文件沒必要使用 TeX ，排長篇且比較挑剔的再 TeX 。

### 遠離版權糾紛
前面提到的其他軟件都是商業軟件，要錢的。如果你是學生或者居住在中國當然無所謂，但若跑到美國去做研究，至少用美國盜版軟件是有風險的。
不過別用商業字體文件，還有如果你的文本編輯器和作圖軟件是商業軟件我也沒辦法。

### 高精度
TeX 本就是個挑剔強迫症患者主持開發的，所以適合高精度排版。軟件設計的時候，精度爲 sp ，什麼概念呢， 65536 sp = 1 pt 。
不過要小心的是現在中國出的宏包一般精度達不到出版級別，還是比不過小日本。
Office 做不到 TeX 的精度， InDesign 做得到但一般用戶也不可能做到。

### 祕書式人機交互
假設你寫了一本曠世巨著，叫你的祕書做成 PDF ，你會怎麼說？
你肯定這麼說的：把大章節給我用一號字、黑體，小章節用三號字、黑體、下劃線，正文用四號字、宋體，奇數頁用大章节標題做頁眉，偶數頁用書名，章節末尾如果是奇數頁就加一頁空白，後面做個人名索引，前面做個目錄，還有參考文獻幫我用 MLA 格式整理一下。
於是祕書打開他的 Word 或者 InDesign ，想着你的吩咐，先把全文設置成四號宋體，然後找到第一章，改成一號黑體，再找到第一章第一節，改成三號黑體下劃線，如此類推。他伸伸懶腰，把各章節頁數找一下，做了一個目錄並逐個改好頁眉和章節末尾，又上網看看 MLA 格式的要求，幫你改好。最後帶着詛咒的心情熬夜一個一個的查了人名，做了索引。
來到 TeX ，你寫文章的時候，寫到大章節，就標記一下，這是大章節；到了人名，再標記一下，這是人名。最後軟件會按照你的構想把需要的樣式排出來。

### 後期調整
回到你和祕書那個 case 。
說不定過了兩天，你又不滿意了，於是對祕書說：小祕，我對宋體有點審美疲勞，你給我把正文和小章節換仿宋，順便開本改 B5 ，參考文獻格式換哈佛。
於是祕書抓狂了。字體重新設置，目錄、索引、參考文獻都要重做……
如果你沒有祕書，抓狂的就是你自己。
所以 Word 和 InDesign 的用戶多半不能對美過於執着，又尤其不能有千變萬化的心情和設計，更不能同一本書有三四種排版。當然，現在 Word 的宏是不錯的，有些東西可以比較方便的批量處理，不至於像前面那位祕書那麼辛苦，比如目錄和索引都是可以自動的。不過前提是你得是 Word 高手，而成爲 Word 高手的人不多於 TeX 高手，就好像高中數學聯賽國三 [^1] 得主不比數學博士多。至少我覺得學個 VBA 就比學 TeX 要難。
在這個 case 中， TeX 衹要在導言區改幾個字，就能讓全文的設計煥然一新了。甚至可以寫好後套用十幾個模板，來個一稿 N 投——來，想像一下，用 Word 寫好後出版社再提要求的感覺該有多噁心，再想想 TeX 的噁心處，你就會覺得，還是 TeX 沒那麼噁心。所以就有了這句話：
bq. I hope to die before I have to use Microsoft Word.

### Device Independent
Device Independent 本來是形容 TeX 的編譯結果 dvi 文件可以在各種設備上打印。不過對於用戶來說，又有不同意義。
現在平板電腦流行，用戶往往經常轉戰多平臺。如果使用商業軟件，難免會在某些平臺下不好書寫。 TeX 就不存在這問題，他是文本文件，手機編輯也不用擔心出問題。
Device Independent 還有一個意義，即，我們可以用任何自己覺得舒服的文本編輯器去處理他，而不必忍受略慢的 Word 或奇慢的 InDesign 。

### 團隊作業與版本控制
Word 也有專門的團隊作業功能，不過各種坑爹，而且團隊作業顯示與作業結果不能並存。版本控制方面， Word 文件卽使使用了外部程序，具體每個版本修改了什麼都不能直觀反映。
TeX 是一堆文本文件，結合 Git 就是當下在程序猿裏最流行的團隊作業與版本控制方式，所有修改都非常淸楚。

### 乾淨
Word 和 InDesign 的文件都較髒。而 TeX 是純文本，除非你自己不講衛生，不然都很乾淨。
什麼叫髒？比如在 Word 把一段話設置爲紅色再藍色再綠色最後改回黑色，然後保存，結果文件竟然變大了，因爲程序在你變一次顏色的時候不是消掉原來的顏色再加上新顏色，而是直接加。 Word 內部也有他的標記語言，比如剛纔的修改，他可能是這樣的：文字——[紅色]文字[紅色]——[紅色][藍色]文字[藍色][紅色]——[紅色][藍色][綠色]文字[綠色][藍色][紅色]——[紅色][藍色][綠色][黑色]文字[黑色][綠色][藍色][紅色]。所以你越改動，文件就越大。

### 擴展性
TeX 是開源軟件，衹要水平夠，你可以用來排任何古怪但有規律的東西。
換句話說，沒有解決不了的問題，只有解決不了問題的人。
當然，如果不是高手，很難搞定一些困難的問題。不過 Plain TeX 已經有了六百個 primitive ， 現在宏包的量又那麼大，低手也想不到太多奇怪的問題。

### 縮寫
其實 TeX 也可以像 html 有 CSS 那樣偷懶的，那就是用戶自定義。你可以把一長串命令定義爲一個斜杠加一對大括號再加若干個字母，甚至可以用一個符號開啓一串命令。

### 裝逼
如果要找出世界上逼格最高的軟件， TeX 自然排名第一。原因是他的用戶基本上全都是學界裏的人，特別西方理工科語境下，如果一個人說不知道 TeX ，可以斷定他的文憑不高於本科。

## TeX 的「競爭對手」
雖然已經羅列了 TeX 的優點，不過還是稍稍對比一下好了。

#### 方正書版
方正書版擁有很多 TeX 的優點，對古籍排版很有一套，發排速度飛快（ TeX 編譯起來眞的相當慢，我編譯），程序也較清爽。那爲什麼我們還要研習 TeX 呢？
TeX 開源。有問題慢慢想還是能解決的，而書版如果沒有某個功能，就衹好乾瞪眼。
用 TeX 能接觸到更多較底層的東西（開源嘛），學習更多知識，增強排版能力，鍛煉堅強心性。
TeX 免費。書版最新的破解版是十多年前的（但完成度、穩定性都很高）， 2008 版價格 6460 人民幣。
TeX 跨平臺。這優勢不很明顯，因爲除了調試、發排沒人整天編譯。
TeX 社區活躍。書版除了 CPC 和方正自己的論壇，幾乎沒人討論。
TeX 精度更高。跟 TeX 比精度那是找死。

#### Adobe InDesign
從「排出來」的角度來講，無所不能。但我就是不想用：
慢。 Adobe 沒有不慢的。
弱爆了的批量操作還沒有 VBA 。 WYSIWYG 的死穴。
商業化。他不會讓你接觸底層的東西，也不會理你的小衆需求。然後你還要找破解。
見鬼了的源文件。書版還能用文本編輯器編輯， InDesign 必須用他自己來編輯。

#### Word
這貨不是排版軟件，你有這功夫折騰 Word 那風騷的時濃時淡的墨色、時大時小的行距、時在此時在彼的插圖、時好時壞的程序，幹嘛不用 Powerpoint 或者 Photoshop 來排書？
雖然很多人喜歡拿來比，不過我認爲沒意義。還不如對比 Word 和 AutoCAD 呢。 Word 就是一款字處理軟件，用來打一份不長的內容應付交差是挺好，不要給他太繁重的勞作。
反正，每次聽到有人建議我用 Word 排書，我就趕快學習一下 TeX 壓壓驚。

#### TeXmacs
本來是用 TeX 構建的，現在獨立出來了。
這貨是 WYSIWYG 軟件，擁有 WYSIWYG 的所有缺點。
軟件啓動較慢，默認版式較醜，如果用來做代數作業還不錯，可惜我沒有代數作業。

## 歧途
TeX 是我見過學習歧途最多的軟件——可能是開源而且龐雜的緣故罷？姑且羅列幾條。

#### 發音
TeX 的發音彷彿世界難題一樣，總是要討論一番。其實很簡單，國際音標是 [tex] [^2]。我看到學過英語的中國朋友在後排舉手，表示不認識這個 [x] ，藉此斷定我老人家的音標寫錯了。
我老人家怎麼會寫錯呢，是你英語老師沒學過完整的國際音標啊。比如他一定不懂 [h] 和漢語拼音的 h 的輔音部分發音上的區別。事實上， [x] 的發音就個漢語拼音的 h 的輔音部分完全相同，讀起來就和「河」去掉「鵝」的音一樣。

#### TeX 很難
對個性不強的人來說， TeX 的難度基本上是體系混亂造成的。基本功能的實現比 html 還簡單。不修 Plain TeX 和 ConTeXt ，單玩 LaTeX 的話，還是挺快上手的。
TeX 也許跟許多用戶所熟悉的體系非常不同，故而彷彿不易掌握。沒關係，一次學不會，刪掉，半年後再學學，再刪掉，再等半年一年。不單是 TeX ，很多事都可以用這種手段處理。

#### 高手纔能用 TeX 排版出複雜 fancy 的東西
學了就是高手。
當然前提是智商沒問題。
大學都考不上就算了。

#### 離開 WinEdt/TeXworks 就不會用 TeX
CTeX 用戶容易犯的毛病，該發行版對二者的設置很好，又不去教用戶如何進一步設置。
這個問題我會在下一部分的「編輯器」小節談到。
如果是中文寫作，用這兩款編輯器是很抓狂的。

#### 使用他人模版
你妹的模版，初學者絕對不該使用！一個模版往往包含將近十個宏包，新手不亂完纔怪！
別人的模版是熟練者需要應付不同格式，或者是製作模版時偷構思用的！

#### 概念混淆
網上經常看到有人自稱用了將近十年 TeX 的，卻搞不清發行版、引擎、編輯器、宏包之間關係。老實講這種人該用商業軟件，而且實在不適合做研究。

## 使用參考
雖然 Plain TeX 也沒有多難，但是 LaTeX 更簡單，可用宏包、命令更多，所以初學一般從 LaTeX 開始比較好。上手後可以再考慮慢慢向其他過渡。

### 幾個入門文檔
<a href="http://www.dralpha.com/zh/tech/lnotes.pdf" rel="external">lnotes</a> <a href="http://www.dralpha.com/zh/tech/lnotes2.pdf" rel="external">lnotes2</a> ，作者姓黃，署名包太雷，個人判斷出生時間不晚於 1970 年，因爲他用了「馬尾巴的功能」 [^3] 的典故。文章風趣詼諧，八卦信手拈來，而且排得較 fancy 。不過他的立場是 XeLaTeX ，直排不如 LuaLaTeX 。
<a href="大家來學 LaTeX" rel="external">http://cle.linux.org.tw/~edt1023/tex/latex123/node1.html</a> ，臺灣李果正撰，對中文的討論過時，不過 LaTeX 基礎都已覆蓋。
很多人認爲 lshort 或其中文版也不錯，個人覺得太囉嗦，僅最後一章有意思。
入門文檔本來不需看太多，但 TeX 很多基本概念必須掌握，多讀幾本入門文檔有助於將之灌入大腦。

### The TeXbook
Knuth 寫給 TeX 初學者的書，但不建議直接就讀他。該書也被廣大低手視爲「傳說中」的書，其實沒這麼恐怖。不關注公式編輯的，可以讀一下 10-15 和 20-25 這些章節，重點理解盒子。
閱讀此書對進一步理解 TeX 宏包中的命令以及製作宏包有很大作用，適合對美有獨特追求的人。

### TeX Reference Manual
Plain TeX 有一堆 primitive ，掌握這些， Plain TeX 當然也就入門了。這本書就是專門講解這些知識點的，不過講得比較粗糙，很多地方還是看 The TeXbook 比較好。
網頁版是 <a href="http://www.tug.org/utilities/plain/cseq.html" rel="external">TeX Primitive Control Sequences</a> 。

### TeXbyTopic
TeX Live 自帶的一篇文檔，也解釋了 primitive ，可與前者互補。

### 方正書版的入門文檔
看這個不會直接有助於學習 TeX ，但可以瞭解中國出版業對版心、行距等方面的習慣。
網上有很多不符合行規的模板，不忍直視。

### A Guide to LaTeX
有點長，可以作爲初級工具書來讀。該書分解了很多命令，比如一個 `\footnote` 包含了 `thefootnote`, `\footnotemark`, `\footnotetext` 等。讀到這本書說明你的要求很多很特殊，一般的模板和各種入門文檔已經不能滿足你了。

### source2e + macros2e
前者包含 LaTeX2e 所有源碼，後者包含常用內部宏。這兩本書的內容都能喫透，堪稱 LaTeX 高手。
這兩個文檔和 lshort 都集成在很多發行版中，所以安裝發行版要記得勾選文檔。用 TeX 的祕訣就是讀文檔，改碼，測試編譯，再讀文檔……

### 其他文檔
基本上，用到什麼就讀到什麼文檔，這是開源軟件亙古不變的道理。
一般文檔和示例都是隨包的，搜一下就有了。比如 Windows 下用 Everything 找文檔，比用 TeX Live 的命令行還方便。

### log
編譯如果出錯， log 往往能給予極大提示。
不過要完全看懂 TeX 的 log ，要先看很多文檔——比如 badness 什麼的。

## 環境

### 引擎
<a href="http://www.ctan.org/topic/engine" rel="external">CTAN</a> 有詳細列表，這裏重點說一下漢字文化圈常提到的。
pdfTeX: 顧名思義，直接轉成 PDF 。
pTeX/upTeX: 日本引擎，後者是 unicode 的。古老且日本國家特殊性強，外人用起來很痛苦。
XeTeX: 對字體很有一套，編譯時後臺直接把中間產物 xdv 轉成 PDF ，所以較方便。
LuaTeX: 吸收 pdfTeX ，支持直轉 PDF 和方便的字體。 Lua 是腳本語言，速度差點。現在發展出 LuaTeX-ja 來（本質上是宏包），方便的同時部分繼承了 pTeX 。

### 包
Plain TeX: Knuth TeX 封裝成包。相關知識掌握後不會過期，且在所有 TeX 引擎上均能使用，缺點是他用起來繁瑣且內建功能少。
LaTeX: 主要是加了文檔類，並留下很好的發展空間。友好且認可度很高，知識保質期也很長。
ConTeXt: LaTeX 內核精煉，功能實現大量依賴宏包，但宏包間常有衝突。而 ConTeXt 是自身強大，以避免宏包衝突的問題——強得有點像商業軟件。
引擎和包搭配，就有了很多編譯方式。比如 pTeX 可以搭配 Plain TeX 和 LaTeX ，搭配後者就變成了 pLaTeX 。

### 發行版
糾結這問題的新手居多。
目前 Windows 下較常用的發行版有 TeX Live, MiKTeX, W32TeX 。其他多是衍生物。
TeX Live: 宏偉的跨平臺發行版，很大，很全，安裝很簡便，適合新手—— Live 都這樣嘛。
MiKTeX: 也很大很全，好多人都根據他來弄發行版。
W32TeX: 小鬼子作品，沒有整體打包下載，東西也不齊，安裝器如 AbTeXInstaller 也不太好用。日本人討論時喜歡以這貨爲例，適合二鬼子和需要日本宏包的。
我的看法：上手用 TeX Live ，學日本或熟練各種配置了用 W32TeX 。
其他發行版見 <a href="http://www.ctan.org/topic/distribution" rel="external">CTAN</a>"

### 編輯器
任何一款合格的文本編輯器都可以編輯並設置編譯。比如常見的 Vim, Emacs, SciTE, Notepad++, EditPlus, EmEditor, UltraEdit, AkelPad... 目前我用 EverEdit 來寫。
日文 <a href="http://oku.edu.mie-u.ac.jp/~okumura/texwiki/" rel="external">TeX Wiki</a> 裏有個「統合環境」，介紹了主流開源文本編輯器的配置方法。
本文給一個該站沒有的例子—— EmEditor 下 upLaTeX 一次性二步編譯爲 PDF：
先寫好一個 bat 文件放在 upLaTeX 的文件夾裏——比如 W32TeX 就是在 bin 文件夾。
```bat
`echo off
uplatex -synctex=1 -jobname="%~n1" -kanji=utf8 -guess-input-enc "%1" && dvipdfmx "%~n1"
```

再在 EmEditor —工具—外部工具—自定義工具下，標題隨便寫，命令寫剛纔那個 bat 的完整路徑，比如我的就是 `D:\W32TeX\bin\pdfuplatex.bat` ，自變量 `$(Path)` ，原始目錄 `$(Dir)` ，如果需要看 log 就勾選 「使用輸出窗」並把編碼設爲 UTF-8 。其實這就是個文本編輯器使用外部工具的典型例子而已。
upLaTeX 設定相對比較複雜，因爲他編譯成 PDF 需要兩步且有一堆參數而且 EmEditor 不是直接調用 cmd 。如果是 LuaTeX ，不用寫 bat 了，直接調用 exe 就行了。
網上也有很多專門針對 TeX 開發的文本編輯器，比如 WinEdt, WinShell, Kile, TeXstudio, TeXnicCenter, TeXworks, SWP, Bakoma 等等，其中有的是商業軟件。我個人的觀點還是用自己喜歡的 general 文本編輯器，而非專門爲 TeX 找，免得不習慣。

## 相關宏包

#### geometry
進一步控制整個頁面佈局的經典宏包，主要是尺寸方面的設計。

#### fancyhdr
製作很 fancy 的頁眉和頁腳。能基於頁面奇偶性來設置不同頁眉、頁腳，但奇偶性必須開啟 documentclass 中的 twoside 選項。

#### color/xcolor
一本書都沒別的顏色嗎？
如果是實際印刷，多色較貴，一般用單色。但電子版多幾種顏色更好，就像我們寫代碼喜歡做高亮。

#### sidenotes/marginnote
LaTeX 內部有一條叫 `marginpar` 的命令，可以製作邊注。
但 marginpar 是浮動對象，所以就有了 marginnote 宏包。同時加了一串不痛不癢的功能。
而 sidenotes 基於 marginnote ，還可以在邊注中加入圖片、表格。

#### titlesec, titleps, titletoc
默認的目錄和章節號是英文的，呆板醜陋。自己動手一下，自然豐衣足食。

#### hyperref
爲 pdf 文件添加超鏈接，等於方便讀者。
這個宏包好像比較容易和別人打架。
目錄默認每個章節一個很醜陋的大框，而且定了顏色之後衹自動給標題變色，不給「第一章」之類的內容變色。

#### fancybox, tikz
如果需要版框，就用這兩個宏包畫一下。這樣看起來就更中式了。

#### ltj-warichu
排割註用的，不很完善，其環境與很多東西衝突。
沒有集成在發行版裏，要自行下載。

## 字體
字體是 TeX 一個重大問題，目前在直排下鼓搗字體相當痛苦。

#### 字符集
如果中文衹有小學水平，一般不用擔心——除非用日本的字體。然而我們的識字量是否有必要稍微提升一些呢？於是字符集問題就來了。
近期來講，中國的字體最少是 GB2312 （業餘字體會根據自己喜好來），大公司出的字體一般有到 GBK ，有時會給到 Unicode 沒有 Ext 。臺灣一般在 Big5 基礎上加點字。日本的字體是 JIS ，老標準是 JIS90 ，較新的是 JIS2004 。
日本人善於制定和遵守規則（這一點我喜歡），重點說一下。很多字體後面常附上表示該字體字符集覆蓋面的標識，比如 Std StdN Plus PlusN Pro ProN Pr6 Pr6N 。日本人把漢字使用頻率分爲六等，覆蓋 1-3 的算 Std ， 1-4 的算 Pro ， 1-5 的算 Pr5 ，1-6 的算 Pr6 。照我的理解，不帶 N 的 CMap 是 JIS90 ，新字形；帶 N 是 JIS2004 ，舊字形。
很顯然，如果使用日本字體，如果不是標榜字多如花園明朝的， Pr6N 爲最善。但是 Pr6N 也缺很多常用字，比如夠、躲、嗯、拋、嚐等。日本貨就是日本貨，不可能完全適應中文環境。

#### 書體
這問題是個重點——如果你是比較 demanding 的人。我就很龜毛，所以我對現有的字體都不滿意。
我個人覺得最好看的書籍字體是仿宋（宋朝體），但現在多數仿宋一排長文就很難看。仿宋不是主流，一般字符集較小，日本的 Iwata Souchou Pro M 稍好，也不能滿足我的日常需求，所見最大的 AdobeFangsongStd-Regular 總有一種很呆板的感覺。
退而求次，宋體（明朝體）也馬馬虎虎，但新字形宋體總覺得太虛。完整的舊字形字體貌似也就那「康煕字典體」，還是個 boundingbox 不正確的貨，排書宛如狗啃。現在暫用 SonyReader Ming [^4] 和 蘋果在用的 Hiragino-Mincho-ProN-W3 （下載不到 Pr6N ， W3 屛幕顯示有點粗，印刷還好）。另外還有個 I.BMing [^5] ，字是非常全了，但還有一些問題。
至於楷書，長文看着累，短文不錯，但還是要看原形和質量。 A-OTF-OutaiKaiStd-Light 的質量是不錯，方正的瘦金也馬馬虎虎，不過楷書字體普遍字少，還是不好用。
行書和草書呢？這兩個我基本上不認爲是印刷體。特別是草書，遊絲引帶怎麼解決？未來有什麼黑科技，那又是另一回事，但我眞的懷疑等到黑科技誕生，已經沒人會寫草書了。
黑體是我最不想用的字體，但現在很多人在電腦上就是喜歡。眞是不明白啊，漢字不就是一種以變化爲美的字嗎？這種所有筆畫寬度都一樣的字體怎麼可能好看？
至於隸書和篆書，這兩個我眞不懂，也沒資格評論。
嘛，總之我很明白 Knuth 爲什麼會寫了 TeX 又寫 METAFONT 。夠情懷就該給自己的書做字體，可是漢字不是衹有 26 個字母那麼簡單，一個個做不知道命有沒有那麼長。現在我一般用日本出的字體爲主。

#### XeTeX/XeLaTeX
要在 XeTeX 直排，須是支持 vertical 命令的字體，一般是 otf 。標點需要完美的 vert 命令，而一般字體不完美。
解決方案：
一、用強大的字體，如 AdobeSongStd-Light.otf ，支持的命令更豐富，可保持標點符號正確性。
二、用更複雜的命令，比如標點一律使用 AdobeSongStd-Light.otf 的標點。

#### LuaTeX-ja
有了 luatexja-fontspec ，字體很好弄。 LuaTeX-ja 環境下直排時字體的問題相對少一點，但仍讓人心煩。

## 常用命令
記錄一下沒有壞處。

### 定義
大到宏的製作，小到自己定一堆便捷命令，都需要用到這裏。
應參看 The TeXbook 第 20 章。
`\def`: TeX, 定義新命令。最常見是 `\def\foo{\bar}` 的樣子，也可以把字符定義成命令，如 `\def|{\bar}` 。有時，命令衹打算作用於很小範圍，想用大括號框起來，可以這樣定義： `\def\foo#1{\bar{#1}}` ，如果有多個變量： `\def\foo#1#2{\bar{#1}\fb{#2}}` ， #1 之類可出現多次，隨你高興。大括號內的東西可以折行以便瀏覽。定義會覆蓋已有命令。定義不能帶有 `\par` ，要 `\par` 需在前面加上 `\long` 。
`\let`: TeX, 讓一個命令等同於另一命令。用法： `\let\foo=\bar` 。
`\newcommand`: LaTeX, 定義新命令。跟 `\def` 很像，可以用 `\par` ，但不能定義 end 開頭的命令，而且如果已有同名命令，則不起效。用法： `\newcommand{\foo}[2]{\bar{#1}\fb{#2}}` 。
`\renewcommand`: LaTeX, 重新定義命令，用來覆蓋已有命令。

### 引入
如果事無巨細全都自己寫，未免太痛苦，所以用點宏包什麼的不要太正常。
自己寫模板來用，爲了方便管理，也會把模板和正文分開——這種做法在方正書板裏甚至是強制的。
`\input`: TeX, 最原始的拉來就用。用法： `\input filename` 或 `\input{filename}` 。
`\include`: LaTeX, 會開新一頁。用法： `\include{filename}` ，默認帶 .tex 擴展名。
`\includeonly`: LaTeX, 同 `\include` 用於引入多文件。用法： `\includeonly{filename1,filename2,...}` 。
`\usepackage`: LaTeX, 套用宏包。如果宏包允許還可寫參數。用法： `\usepackage[optional]{thepackage}` 。
`\documentclass`: LaTeX, 套用一個文檔類。用法： `\documentclass[optional]{theclass}` 。

### 盒子
TeX 在設好後，會自動拆行拆頁各種拆，盒子的基本功能是把一串東西裝起來，不許拆。中文盒子的槪念不很強，因爲一個字就像一個盒子，一般不會拆分。西文詞一般不拆，但太長的也可以拆了用連字符，所以盒子槪念的提出與西文環境有關。
可參看 The TeXbook 第 11 章。
`\hbox`: TeX, 橫向不拆的盒子。用法： `\hbox{foobar}` 。
`\vbox`: TeX, 縱向不拆的盒子。用法： `\vbox{foobar}` 。
`\setbox`: TeX, 註冊盒子，盒子編號從 0 到 255 （很像 `\def` ）。用法： `setbox0=\vbox{foobar}` 。
`\box`: TeX, 使用並淸空註冊的盒子。用法： `\box0` 。
`\mbox`: LaTeX, 什麼都沒有的盒子。用法： `\mbox{foobar}` 。
`\fbox`: LaTeX, 帶框的盒子。用法： `\fbox{foobar}` 。
`\makebox`: LaTeX, 功能盒子，可以設定寬度、對齊。用法： `\makebox[100pt][c]{foobar}` ，其中 c 表示居中，還可以是 l, r, s ，分別表示靠左、靠右、分散。
`\framebox`: LaTeX, `\makebox` 基礎上多個邊框。
`\rotatebox`: LaTeX, 旋轉。用法： `\rotatebox[origin=c]{55}{foobar}` 。 55 是角度，中擴號裏的內容可選的就比較多了。如 origin 可以選 l, r, c, t, b, B ，其中 B 是 baseline ，其他都好猜；還可以寫 x=100, y=200 這種，是以左下角爲原點畫的座標；還有一個參數 units 是設弧度的，平面幾何學得好的可以試試。
`\scalebox`: LaTeX, 縮放。用法： `\scalebox{0.5}[1.5]{foobar}` ，前一個數是水平縮放，後一個個是垂直縮放。

### 位移與粘連
位移如果可以寫數字，這些數字都是可以正也可以負的。這些數字後面通常要帶單位，單位可以是 pt, pc, in, bp, cm, mm, dd, cc, sp, em, ex 。
單位的解釋在 The TeXbook 第 10 章，粘連是 12 章。
h 開頭的換成 v 開頭就是縱向，不專門寫了（懶）。
`\noindent`: TeX, 使當前行、段無縮進。用法：照寫。
`\parindent`: TeX, 設置後文的段落縮進。用法： `\parindent=0em` 。
`\raise`: TeX, 上移。用法： `\raise1emfoobar` 。
`\raisebox`: LaTeX, 上移。用法： `\raisebox{1em}{foobar}` 。
`\kern`: TeX, 右移，定長，不可換行，到了邊緣就凸出去。用法： `\kern1emfoobar` 。
`\hskip`: TeX, 右移，可伸展，可換行。用法： `\hskip1em` 。
`\hfil`: TeX, 向右塡充，相當於讓命令兩側的字符對齊兩側邊緣。用法：照寫。
`\hfill`: TeX, 向右塡充，阻斷 `\hfil` ，而不被 `\hfil` 阻斷，相當於升級版。
`\hfillneg`: TeX, 也就是 `\hfill` 的負數。

## Dirty Hacks
從一個 Word 用戶的視角來看，希望某個字符出現在頁面的某個位置是件很簡單的事——開一個文本框，放進去，用鼠標調整一下就好了嘛。當然了， TeX 用戶也可以用命令做類似的事情，但 TeX 用戶通常還希望使用了一個命令後，所有類似情況都自動執行，不需要更多的人工干預。
直排很特殊，很多問題暫時沒有完美解，於是我就利用類似 Word 視角但基本上不用再加人工干預的方式解決。不過，有時解決得很糟糕，那又是另一回事了……
這裏就是其記錄。

### 直排標點
一般情況下， vert 可以使大部分標點符號看起來正常些，但也有些符號死不悔改，非要強制糾正。
對於 ttf 字體，我們往往就束手無策了，需要借用 otf 字體來改。

#### 冒號
冒號在直排下本來和橫排看起來一樣，但是很多字體加了 vert 會睡下來。這就需要專門爲冒號指定字體，但直接切換字體必然導致源文件看起來很醜且輸入麻煩，比如把冒號寫成 `{\sung{：}}` （這還是設置過字體以後，比較簡潔的寫法了）。
這對平時以源文件編輯及檢閱爲主的本人根本不能忍，於是決定在導言區申明。然而卽使用 `def` 命令，也最多衹能做到每次輸入冒號時寫作 `\：` ，還是不能忍，於是就把冒號用 `active` 寫進控制序列去了。

#### 破折號
破折號的編碼有好幾種。
U+2014 是最正確的，但他在直排情況下很多字體顯示爲橫的。
U+FE31 是專排直排的，顯示沒問題，但源文件肯定不會這麼寫。
U+2500 是劃線符號，不過看起來和破折號很像，而且很多字體裏要橫便橫要豎便豎。
U+2015 兩根線之間有明顯縫隙，但也勉強能用
問題雖然可以解決，卻也和冒號的情況一樣。

#### 引號
可能是 box 的緣故，引號普遍靠上，本來應該顯示爲「這樣」的，卻有點像是「 這樣」，看起來很不舒服。
於是在控制序列定的命令裏又加上了 `\kern0.3em` ，動到盒子，後面又用 `\kern-0.3em` 改回。
所以說我寫的代碼處女座看了眼睛會瞎。

#### 專名與書名
專名用直線、書名用波浪線，這是比較好看的標點。以前由於波浪線難弄，改成了俄文引號，現在大可恢復。不過，在直排 TeX 的世界裏，這又是一件大工程。
ulem 是個鼓搗下劃線的宏包。但在中文環境下不自動折行。
CJKulem 提供了中文環境下劃線文字的自動折行，運行需要 ulem 。不過 XeTeX 直排時基線是錯的，所以劃線的位置也是錯的。況且他的直排在左邊，不在我喜歡的右邊（我的習慣很日本是不是）。
udline 是日本人做的，不但有下劃線，還有上劃線，且在 pTeX 環境下自動適應爲下劃線在右側。但是在 XeTeX/XeLaTeX 下不整齊，在 LuaTeX-ja 環境下不能完美適應直排（比如波浪線是橫着的）。
搞半天發現，還是 udline 這塊爛泥較可能糊上牆，於是改了一句代碼，能在直排下用專名和書名就行了，其他不管。

#### 位置
雖然一般是放右上角，直排還是居中較美觀。特別是圓嘟嘟的句號，放中間多對稱啊。
xeCJK 下可以用 `MiddlePunct` ，但 LuaTeX 不能用這個包。哪天心情好我做個字體，再把更多標點符號放進控制序列裏好了……

### 「一」字
在 LuaTeX-ja 直排裏，「一」字的位置不知什麼原因上移了 0.3em 。
使用控制序列修正後，用 `\kansuji` 轉的頁碼、章節名還是錯的。
給字體加上 `[NoEmbed]` 屬性也可以，但我覺得能 embed 到 pdf 更好。

## 有用的網站
<a href="http://www.ctan.org/" rel="external">CTAN</a> <a href="http://www.tug.org/" rel="external">TUG</a> 宏包、文檔、發行版大全。當然，不會太全。
<a href="http://www.latex-project.org/" rel="external">LaTeX 官網</a>
<a href="http://en.wikibooks.org/wiki/LaTeX" rel="external">Wikibooks - LaTeX</a>
<a href="http://texdoc.net/" rel="external">TeXdoc online</a>
<a href="http://oku.edu.mie-u.ac.jp/~okumura/texwiki/" rel="external">TeX Wiki</a> 日本人寫的 Wiki 式網站。
<a href="https://www.sharelatex.com/" rel="external">ShareLaTeX</a> 在線寫 LaTeX 項目，自用免費，文檔豐富。等於免環境用 LaTeX 。


[^1] 先初賽，再省級聯賽，各省省一前若干名可參加全國聯賽，全國聯賽參加人數約一百。聯賽的作用在於選拔人員參加國際奧數「爲國爭光」，有特定題型和知識範圍。卽使是天才，若不高強度備考，國三無望。
[^2] 這是英式英語的發音，美式英語當作 [tɛx] （要顯示中間這個字符需要字體支持）。筆者的耳朵和嘴巴都無法區分 [e] 和 [ɛ] 這兩個音，衹能通過看 IPA chart 看出是嘴巴張開幅度不同。中國很長一段時間都以英式英語作爲標準英語進行敎學（從語言而非交流角度來講這也是正確的），小夥伴們將就着看罷。
[^3] 典故來自 1975 年的電影「決裂」，講述一個南方的大學，學生想瞭解養牛的農技，但教授堅持學術，講授南方較少的馬，而且電影爲了諷刺教授，專說這名教授在講「馬尾巴的功能」。電影的思想是極左的，認爲大學不如農田，學術不如經驗，「馬尾巴的功能」當然不如如何養牛重要——其實這些學生根本不該上大學，職高比較適合他們。這種思想在改革開放後受到完全的否定，因此其後觀看此片的人極少。筆者也是因一個偶然的機會看到了電影的大綱，纔下載來看的。在此筆者順帶將此片推薦給青年及外籍中國史研究者，相信大家一定會喜歡。
[^4] 字符集達到 Unicode CJK+Ext-A ，是目前能用的舊字形字體裏最大的。網上有根據他修改的「宋明體」，頗有點名氣。然而修改者似乎不知 Ext-A ，又似乎和簡化字有仇，強行亂改了很多字，流毒不淺。我一直奇怪，「宋明體」除了那些白癡問題以外，製作精良，字形一致，不太可能是單槍匹馬的業餘人士製作，就很想找源頭，但是修改者完全刪掉了字體原有的信息，發帖時又不指出所據字體，很長時間都沒找到。最後機緣巧合，終於發現是 Sony Reader 上的字體。而且這套字體還有楷、隸、黑三體，衹有楷體無 Ext-A ，實在難得。
[^5] 修改自 IPAmjMincho ，收字達到了 Ext-D 。但不知是字體精度不夠還是什麼緣故，總覺得不太平滑，而且他對所有在編碼上區分了新舊字形的字一律採用舊字形，這有時會讓用戶感到困擾。