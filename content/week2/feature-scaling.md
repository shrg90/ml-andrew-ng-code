---
title: "Feature Scaling"
date: 2020-09-09T21:48:49+04:30
draft: false
weight : 30
---

در این قسمت و قسمت بعدی در مورد فوت و فن هایی 
برای اعمال الگوریتم گرادیـــان کـــاهشی صحبت می‌کنیم.

اگر شما مسئله ای دارید که چندین ویژگی یا متغیر دارد
و اگر مطمئن هستید که متغیر ها در مقیاس مشابه ای
نسبت به هم هستند، در این حــالت گرادیــــان کـــاهشی
با سرعت بیشتری به همگرایی می‌رسد.

فرض کنید مسئله ما دو متغیر به صورت زیر دارد:
$$ x_1 = \text {size(0-2000 feet^2) }$$
$$ x_2 = \text {number of bedrooms(1-5) }$$

که اگر بـخواهیم نــــمودار کــــانتور را رسم کـنیم به این
شکل خواهد شد.
شکلی بلند و بیضی مــانند که گرادیـــان کـــاهشی بـرای 
پیدا کردن مینیمم کلی در این تابع هزینه زمان زیادی 
را باید صرف کند!

![image66.png](../images/image66.png?width=15pc)

**که اینجا از تکنیک Feature Scaling  استفاده می‌کنیم!**

برای انجام این کار باید مقدار متغیر $x$ را بر تفـــاضـل 
کران بالا و پایین خودش تقسیم کنیم.
که با این کار مقادیر متغیر ها عددی بین $0$ و $1 $
قرار می‌گــیرد، و شکل معقول تری خـــواهیم داشــت.
مثلا در این مسئله داریم:

$$ x_1 =  \frac {\text {size(feet^2)} } {2000}$$
$$ x_2 = \frac  {\text {number of bedrooms} } {(5-1)}$$

![image70.png](../images/image70.png?width=15pc)

همچنین روش مشابه دیگری برای انجام این کار به 
اسم mean normalization داریم.
که در صورت کسر، تفاضل مقدار متغیر با میانگین 
همه مقادیر متغیر $x$ را قرار می‌دهیم.

$$ x_i := \frac{x_i - \mu_i} {s_i} $$

{{% notice note %}}
نکته: همچنین در مخرج کسر مـی‌توانیم از مــقدار
انحراف معیار استفاده کنیم، که البته نتایج متفاوتی 
با هم دارند.
{{% /notice %}}