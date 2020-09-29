---
title: "گرادیان کاهشی قسمت سوم"
date: 2020-09-09T17:40:28+04:30
draft: false
weight : 100
---

در این قسمت گرادیان کاهشی را با تابع هزینه ترکیب
می‌کنیم و الگوریتم رگرسیون خطی را به دست می‌آوریم.
تا اینجای کار به این ها رسیدیم:

![image47.png](../images/image47.png?width=40pc)

اینجا می‌خواهیم از گرادیان کاهشی برای مینیمم کردن
تابع هزینه استفاده کنیم!
ابتدا تابع $J$ را در الگوریتم گرادیان جاگذاری می‌کنیم و ...

با محاسبه عبارت مشتق جزئی در گرادیان کاهشی برای
دو پارامتر $\theta_0$ و $\theta_1$ خواهیم داشت:

$$ \theta_0, j = 0: \frac{\partial}{\partial \theta_j} J(\theta_0, \theta_1) = \frac{1}{m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)}) $$

$$ \theta_1, j = 1: \frac{\partial}{\partial \theta_j} J(\theta_0, \theta_1) = \frac{1}{m} \sum_{i=1}^m (h_\theta(x^{(i)}) - y^{(i)}) \cdot x^{(i)} $$

به الگوریتم گرادیان کاهشی بر‌ می‌گردیم و جایگذاری،
و در واقع به الگوریتم رگرسیون خطی می‌رسیم!

![image49.png](../images/image49.png?width=35pc)

در قسمت اول گرادیان کاهشی در مثال موتور سوار
دیدیم که بسته به اینکه از کجا شروع کنیم ممکن است
که به مینیمم موضعی برسیم!
اما تابع هزینه برای رگرسیون خطی همیشه تابعی سهمی
مانند مثل این است:

![image22.png](../images/image22.png?width=25pc)

این تابع محدب مینیمم
موضعی ندارد، و فقط
یک مینیمم کلی دارد.
یعنی گرادیان کاهشی
برای این تابع هزینه
همیشه به نقطه بهینه می‌رسد!
و بنابراین گرادیان نزولی را در عمل برای داده خانه ها به
به این صورت می‌بینیم، که نتیجه تناسب خوبی دارد:

![image51.png](../images/image51.png?width=35pc)

و حالا می‌توانید از آن استفاده کنید تا قیمت خانه ها
را برای دوستانتان پیشبینی کنید!