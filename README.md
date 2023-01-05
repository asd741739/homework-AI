# BigGAN with CLIP, the "Big Sleep"
# 介紹
BigGAN 是一種GAN(Generative Adversarial Network 對抗生成網路)的模型，可用於生成高仿真圖片，
CLIP則是一種人工神經網路，專門用於解讀文字裡所帶有的影像概念，
兩者的結合便是此程式"Big Sleep"，可實現讓使用者可以用簡單的文字來直接取得與文字內容有關的圖片。

本文將介紹如何使用Colab來進行Big Sleep實作。

# 實作
1. 用Colab打開程式代碼，從左邊的目錄切換至Parameters的部分。

第四行的內容:![image](https://user-images.githubusercontent.com/52593926/210743884-106f514c-4953-4764-b227-684bd4e68952.png)

"A photh of dog"的部分就是要轉成圖片的文字內容，可以隨意更改，請注意不要動到撇號(')

更改文字的規則請參照下方"注意事項(1)"

2. 使用Ctrl+f找到" if itt % 100 == 0: "
 
 ![image](https://user-images.githubusercontent.com/52593926/210746614-1aa99150-244a-453f-b023-9592202992af.png)
 
 數字100代表執行時會生成的圖片總張數，可自由更改，免費版建議改成5或以下以避免錯誤。
 
3. 沒問題就可以執行所有儲存格了。

4. 執行完畢後會在Train的部份看到結果。

若結果並不理想，可以利用Diagnostics的部分來進行測驗。

這裡可以直接對參數做出更改，也會提供表格來做分析。


![image](https://user-images.githubusercontent.com/52593926/210748526-4e4be422-209f-4664-9d8a-b5b3dfb79daa.png)


![image](https://user-images.githubusercontent.com/52593926/210748434-89883fc2-edac-4e0c-b4fb-5c1f63cf4d65.png)

 # 注意事項
 
(1) 由於此程式尚在Beta階段，關於命名最好參照以下格式來得到最好的效果:

簡易寫法:A photo of (某種東西)，中文程式無法辨認，請使用英文。

詳細寫法:A (IMG-TYPE) of (SUBJ) in the style of (STYLE)

IMG-TYPE: 指定要輸出甚麼樣的圖片，例如圖畫、素描或雕塑作品等等


SUBJ: 要模擬的主要物件或情況，比如說"three dogs(三隻狗狗)"或者"Arnold Schwarzenegger(阿諾·史瓦辛格)"
可以進一步描述，像是"Arnold Schwarzenegger holding a duck under the moon" (阿諾在月光下抓著一隻鴨子)


STYLE: 非必要，如果說想要模仿某藝術家的風格或某種畫風再來填寫這個。

最完整的例子: "a photograph of Arnold Schwarzenegger holding a duck under the moon in the style of Rembrandt"

(2) 輸出圖片時會有提示聲，請不要被嚇到。

(3) 第一張圖都很不準確，第二張應該是足夠清晰了，生成張數越多理論上會越準確。

# Source

[BigGAN by Andrew Brock](https://arxiv.org/abs/1809.11096)

[CLIP by openAI](https://openai.com/blog/clip/)

[Big Sleep by @advadnoun on Twitter](https://twitter.com/advadnoun)




