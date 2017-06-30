# PTT 中文語料

嗨，這裡是 PTT 中文語料集，蒐集自 PTT 八卦版於 2015 年至 2017 年 6 月的文章，我透過[某些假設與方法](https://github.com/zake7749/PTT-Chat-Generator)將每篇文章化簡為問答配對，其中問題來自文章的標題，而回覆是該篇文章的推文。
可惜的是目前這份資料集的噪聲還有點大，如果您有更棒的方法能提取文章出問答配對，或發現這份資料集有什麼能改進的部份，還請與我聯繫，也祝各位開發順利 :>

## 資料格式

資料集放置於 `data` 中，每一行都是一個問答配對，問與答之間以一個 tab (`\t`) 區隔開，比如說:

```
matlab有什麼炫砲一點的圖？	一樣的圖改一改顏色，有點半透明感覺更唬爛炫
有沒有情人節吃什麼cp值最高的八卦	吃屎啊廢話 免費的一餐
姆咪一個人守得住街亭嗎?	引來一堆肥宅穢土轉生 有機會喔
有沒有被落石砸到該反省的八卦	蔡英文執政就故意誇大報導 東森不意外
情人節該帶女朋友去哪慶祝？	用了一整年 對她好一點  送專業乾洗店吧
為什麼 聖結石 會被酸而 這群人 不會？	質感 劇本 成員 都差很多好嗎 不要拿腎結石來污辱這群人
為什麼慶祝228會被罵可是慶端午不會？	因為屈原不是台灣人，是楚國人。
有沒有戰神阿瑞斯的八卦?	爵士就是阿瑞斯 男主角最後死了
理論與實務最脫節的系	哪個系不脫節...你問最不脫節的簡單多了...
為什麼PTT這麼多人看棒球	肥宅才看棒球　系壘一堆胖子
為什麼達摩祖師傳那麼好看?	達摩從頭到尾都是被動 (別人問他問題
3D小畫家有人會畫嗎？	3D小當家有人會畫嗎
對天龍人來說宜蘭4南部還４東部	他國事務..
機車推出uber或計程機車會怎樣	載到肥宅會很痛苦
台中的龍邦世貿有人跳樓?	曾經當過全台第一高樓，可惜不到一年
抽到海陸會被笑娘炮兵嗎	還好啦，海陸下基地常態，下好下滿。
國高中的國文	你沒看美國考GRE GMAT都要考高深的英文
最經典的老電影?	大國民  火車撞月球 美國新玫瑰情
麥香 阿薩姆 立頓 誰是奶茶界霸主	義美和午後都不錯，但大輸手搖
你們喜歡吸包子嗎？	喜歡啊，吃的時候一定要先啾啾裡面的湯汁。
有沒有便利商店便當飯越來越少的八卦？	沒什麼東西可以吃才會選超商.....
```

目前資料集中共有 418202 筆問答配對，但並不是所有配對都是有效的，因為有些文章並沒有推文，這類問題的回覆會被標記為`沒有資料`(共有 650 筆)，使用時還請注意。

## 探索資料集

`Explore-Gossiping-Dataset.ipynb` 提供了資料集的基本資訊，而 `Intro-to-DataLoader.ipynb` 中介紹了本資料集附帶的一個 `data_loader` 的基本功能
