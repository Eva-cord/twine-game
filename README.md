:: Start
我：「終於下課了！」

今天是我入學的第一天，課堂上老師列了一張清單，說這些是下次上課要用的東西，所以我一放學就到魔法商店街來購買啦。

我：「來看看需要什麼呢~」

材料清單：
- 老鼠的眼睛
- 魔法棒(不限材質)
- 一本魔法藥劑學的課本
- 森林中矮人的頭髮
- 巨鳥的眼淚


在商店街遇到了室友艾蜜莉，她也要去買下次上課要用的東西。

艾蜜莉：「那我們一起吧！」

[[走進魔杖店->魔杖店]]
你走進魔杖店，看到各式各樣的魔杖。


---

:: 魔杖店
我們走到了魔杖店前，裡面有各式各樣的魔法棒，我們在這裡挑選自己喜歡的魔法杖。

選一支魔杖：
* [[石頭製的->書店]]
* [[木頭製的->書店]]
* [[鋼鐵製的->書店]]
* [[不明肉做的->書店]]

（前三個選項愛蜜莉都會說選得不錯，第四個她會驚恐地看你，但都可以完成這關。）

---

:: 書店
來到了書店，在這裡可以找到老師指定的課本。

你想拿哪本書？
* [[生命學之書->結局1]]
* [[惡魔召喚之書->結局1]]
* [[魔法藥劑學課本->雜貨店]]
* [[成人之書->結局1]]

---

:: 結局1
你沒有辦法交到新朋友艾蜜莉，之後的學校生活皆被排擠，一個人孤獨地上學。

THE END（結局1）

---

:: 雜貨店
來到雜貨店，可以買到老鼠的眼睛、巨鳥的眼淚。

這裡你需要完成兩個拼圖（想像成小遊戲），有三次機會完成。  
如果三次內完成：[[繼續前往森林->森林]]

失敗：[[結局2]]

---

:: 結局2
你沒有辦法交到新朋友艾蜜莉，雖然會交到其他朋友，但之後不會再和艾蜜莉講話。

THE END（結局2）

---

:: 森林
現在商店街沒有賣「矮人的頭髮」，所以你和艾蜜莉一起到岩石森林去尋找矮人。

這關卡是以「好感度」為基礎，請依序做出四次選擇（最少加到85才算成功）。

[[開始與矮人對話->矮人第一回合|score=0]]

---

:: 矮人第一回合
矮人：「你們是誰？為何來這裡？」

* [[「廢話少說！你頭髮我全都要了！」->矮人第二回合|score+35]]
* [[「您好！矮人先生我們想請你幫我們一個忙！……」->矮人第二回合|score-25]]
* [[默默拿出一小袋銅幣->矮人第二回合|score+20]]

---

:: 矮人第二回合
矮人：「所以你們是想要我的頭髮對吧，我憑什麼要給你們！」

* [[「臭老頭！趕緊把頭髮交出來！」->矮人第三回合|score+25]]
* [[「矮人先生，我們真的很需要您的頭髮……」->矮人第三回合|score-10]]
* [[默默拿出一袋銀幣->矮人第三回合|score+25]]

---

:: 矮人第三回合
矮人在思考中……

* [[直接揍矮人->矮人最終回合|score-35]]
* [[「超級帥氣矮人先生，您就算沒頭髮也帥氣！」->矮人最終回合|score+20]]
* [[默默拿出一袋金幣->矮人最終回合|score+35]]

---

:: 矮人最終回合
矮人：「好吧！我同意了，但你們要給我什麼？」

* [[直接拔下兩根頭髮->檢查好感度|score+10]]
* [[「我們會寫1000字感謝信」->檢查好感度|score-35]]
* [[拿出一罐強效生髮藥水->檢查好感度|score+35]]

---

:: 檢查好感度
(if: $score >= 85)[
    [[完成所有任務->HappyEnd]]
]
(else:)[
    [[任務失敗->結局3]]
]

---

:: HappyEnd
兩人都買到了明天上課要用的物品，一起開心上課，主角也交到了學校裡的第一個朋友！

🎉 Happy End 🎉

---

:: 結局3
你與艾蜜莉成為了朋友，但因為你們沒有找到上課所需要的用品，兩人在課堂上被老師罵了。

THE END（結局3）
