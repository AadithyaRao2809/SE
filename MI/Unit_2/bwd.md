### The Chain Rule
![](../../Attachments/bwd-20230924-9.png)
![](../../Attachments/bwd-20230924.png)
$$1)\;\frac{\partial L}{\partial{\hat{y}}}$$
$$2) \; \frac{\partial{\hat{y}}}{\partial{O_{11}}}$$
$$3) \; \frac{\partial{\hat{y}}}{\partial{O_{12}}}$$
Then find the other derivatives

![](../../Attachments/bwd-20230924-10.png)
*green box is common*

**1)** ![](../../Attachments/bwd-20230924-11.png)
**2)** ![](../../Attachments/bwd-20230924-12.png)

**1 x 2 :**
$\frac{\partial L}{\partial Z}=-(y-\hat{y})$

![](../../Attachments/bwd-20230924-13.png)
![](../../Attachments/bwd-20230924-14.png)
![](../../Attachments/bwd-20230924-15.png)

[Multi Class bwd](bwd_multi.excalidraw.md) 
![../../Attachments/bwd2023-09-27,21.19.57.excalidraw.svg](../../Attachments/bwd2023-09-27,21.19.57.excalidraw.svg)a
%%[[../../Attachments/bwd2023-09-27,21.19.57.excalidraw.md|🖋 Edit in Excalidraw]], and the [[../../Attachments/bwd2023-09-27,21.19.57.excalidraw.dark.svg|dark exported image]]%%
![](../../Attachments/bwd-20230924-16.png)

Start backwards and memoize, later derivatives will be used, no need to calculate



