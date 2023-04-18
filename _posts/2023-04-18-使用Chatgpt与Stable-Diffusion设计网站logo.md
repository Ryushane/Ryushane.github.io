![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-1](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-1_10-49-58.png)
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-2](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-2_10-49-58.png)
接下来把这些关键词放到Prompt中，有选择性地删除或增加keyword。比如Geek效果就不怎么好，删了换成hexagon等抽象多边形。在这里我加入了<lora:lightAndShadow_v10:1> <lora:lightlineArtLora_v10:1>这两个光影lora，让光影效果更符合我的喜好。
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-3](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-3_10-49-58.png)
把batch size和batch count都调大一些，方便自己挑选。
接着就得到了一大堆512╳512尺寸的图片，选一些从缩略图上看就很有标识性的。
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-7](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-7_10-49-58.png)
最终效果我觉得还不错的有下面这些：
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-4](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-4_10-49-58.png)
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-5](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-5_10-49-58.png)
![2023-04-18-使用Chatgpt与Stable-Diffusion设计网站icon-20230418-6](https://cdn.jsdelivr.net/gh/Ryushane/PicGo_Pictures/img/2023/04/18/2023-04-18-%E4%BD%BF%E7%94%A8Chatgpt%E4%B8%8EStable-Diffusion%E8%AE%BE%E8%AE%A1%E7%BD%91%E7%AB%99icon-20230418-6_10-49-58.png)
但其实这些logo想拿来做icon还是太复杂了，可以考虑后续用control net简化。