---
title: "مطالعه موردی: نخستین تصویر از یک سیاه‌چاله"
sidebar: false
---

{{< figure
  src="/images/content_images/cs/blackhole.jpg"
  title="Black Hole M87"
  alt="black hole image"
  attribution="(Image Credits: Event Horizon Telescope Collaboration)"
  attributionlink="https://www.jpl.nasa.gov/images/universe/20190410/blackhole20190410.jpg" >}}
{{< /figure >}}

{{< blockquote
  cite="https://www.youtube.com/watch?v=BIvezCVcsYs"
  by="Katie Bouman, _Assistant Professor, Computing & Mathematical Sciences, Caltech_"
>}}
Imaging the M87 Black Hole is like trying to see something that is by definition impossible to see.{{< /blockquote >}}

## یک تلسکوپ به اندازه زمین

The [Event Horizon telescope (EHT)](https://eventhorizontelescope.org) is an
array of eight ground-based radio telescopes forming a computational telescope
the size of the earth, studing the universe with unprecedented
sensitivity and resolution.  The huge virtual telescope,  which uses a technique
called very-long-baseline interferometry (VLBI), has an angular resolution of
[20 micro-arcseconds][resolution] — enough to read a newspaper in New York
from a sidewalk café in Paris!

[resolution]: https://eventhorizontelescope.org/press-release-april-10-2019-astronomers-capture-first-image-black-hole

### Key Goals and Results

- **A New View of the Universe:**
  The groundwork for the EHT's groundbreaking image had been laid 100 years
  earlier when [Sir Arthur Eddington][eddington] yielded the first
  observational support of Einstein's theory of general relativity.

- **The Black Hole:** EHT was trained on a supermassive black hole
  approximately 55 million light-years from Earth, lying at the center
  of the galaxy Messier 87 (M87) in the Virgo galaxy cluster. Its mass is
  6.5 billion times the Sun's. It had been studied for
  [over 100 years](https://www.jpl.nasa.gov/news/news.php?feature=7385), but never before
  had a black hole been visually observed.

- **Comparing Observations to Theory:** From Einstein’s general theory of
  relativity, scientists expected to find a shadow-like region caused by
  gravitational bending and capture of light. Scientists could
  use it to measure the black hole's enormous mass.

[eddington]: https://en.wikipedia.org/wiki/Eddington_experiment

### The Challenges

- **Computational scale**

  EHT poses massive data-processing challenges, including rapid atmospheric
  phase fluctuations, large recording bandwidth, and telescopes that are
  widely dissimilar and geographically dispersed.

- **Too much information**

  Each day EHT generates over 350 terabytes of observations, stored on
  helium-filled hard drives. Reducing the volume and complexity of this much
  data is enormously difficult.

- **Into the unknown**

  When the goal is to see something never before seen, how can scientists be
  confident the image is correct?

{{< figure
  src="/images/content_images/cs/dataprocessbh.png"
  title="EHT Data Processing Pipeline"
  alt="data pipeline"
  align="center"
  attribution="(Diagram Credits: The Astrophysical Journal, Event Horizon Telescope Collaboration)"
  attributionlink="https://iopscience.iop.org/article/10.3847/2041-8213/ab0c57" >}}
{{< /figure >}}

## نقش NumPy

اگر مشکلی در داده‌ها وجود داشته باشد چه می‌شود؟ یا شاید یک الگوریتم بیش از حد به یک فرضیه خاص متکی باشد. آیا با تغییر یک پارامتر، تصویر به طور چشمگیری تغییر خواهد کرد؟

همکاری EHT این چالش‌ها را با تشکیل تیم‌های مستقل برای ارزیابی داده‌ها و استفاده از تکنیک‌های بازسازی تصویر هم سنتی و هم نوین، برطرف کرد. هنگامی که نتایج یکسان بودند، آن‌ها را ترکیب کردند تا نخستین تصویر از سیاه‌چاله را به دست آورند.

کار آن‌ها نقش اکوسیستم علمی پایتون را در پیشبرد دانش از طریق تحلیل داده‌های مشارکتی نشان می‌دهد.

{{< figure
  src="/images/content_images/cs/bh_numpy_role.png"
  alt="role of numpy"
  title="The role of NumPy in Black Hole imaging" >}}
{{< /figure >}}

For example, the [`eht-imaging`][ehtim] Python package provides tools for
simulating and performing image reconstruction on VLBI data.
NumPy در هسته پردازش داده‌های آرایه‌ای که در این کتابخانه استفاده می‌شود قرار دارد، همان‌طور که نمودار وابستگی نرم‌افزار جزئی زیر نشان می‌دهد.

{{< figure
  src="/images/content_images/cs/ehtim_numpy.png"
  alt="ehtim dependency map highlighting numpy"
  title="Software dependency chart of ehtim package highlighting NumPy" >}}
{{< /figure >}}

[ehtim]: https://github.com/achael/eht-imaging

Besides NumPy, many other packages, such as
[SciPy](https://scipy.org) and [Pandas](https://pandas.pydata.org), are part of the
data processing pipeline for imaging the black hole.
The standard astronomical file formats and time/coordinate transformations
were handled by [Astropy][astropy], while [Matplotlib][mpl] was used
in visualizing data throughout the analysis pipeline, including the generation
of the final image of the black hole.

[astropy]: https://www.astropy.org/
[mpl]: https://matplotlib.org/

## Summary

آرایه چندبعدی کارآمد و انعطاف‌پذیر که ویژگی اصلی NumPy است، به پژوهشگران این امکان را داد تا مجموعه داده‌های عددی بزرگ را مدیریت کنند و زمینه‌ای برای نخستین تصویر از یک سیاه‌چاله فراهم آورد. یک لحظه تاریخی در علم که شواهد بصری خیره‌کننده‌ای از نظریه اینشتین ارائه می‌دهد. این دستاورد نه تنها شامل پیشرفت‌های فناورانه است، بلکه نتیجه همکاری بین‌المللی بیش از ۲۰۰ دانشمند و برخی از بهترین رصدخانه‌های رادیویی جهان نیز می‌باشد.  الگوریتم‌های نوآورانه و تکنیک‌های پردازش داده که مدل‌های نجومی موجود را بهبود بخشیدند، به کشف یکی از رازهای جهان کمک کردند.

{{< figure
  src="/images/content_images/cs/numpy_bh_benefits.png"
  alt="numpy benefits"
  title="Key NumPy Capabilities utilized" >}}
{{< /figure >}}
