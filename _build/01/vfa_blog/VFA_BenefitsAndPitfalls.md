---
redirect_from:
  - "/01/vfa-blog/vfa-benefitsandpitfalls"
interact_link: content/01/vfa_blog/VFA_BenefitsAndPitfalls.ipynb
kernel_name: sos
title: 'Benefits and Pitfalls'
prev_page:
  url: /01/vfa_blog/VFA_DataFitting
  title: 'Data Fitting'
next_page:
  url: /01/vfa_blog/VFA_References
  title: 'References'
comment: "***PROGRAMMATICALLY GENERATED, DO NOT EDIT. SEE ORIGINAL FILES IN /content***"
---

## Benefits and Pitfalls

<p style="text-align:justify;">
It has been well reported in recent years that the accuracy of VFA T<sub>1</sub> estimates is very sensitive to pulse sequence implementations (Stikov et al. 2015; Lutti & Weiskopf 2013; Baudrexel et al. 2018), and as such is less robust than the gold standard inversion recovery technique. In particular, the signal bias resulting from insufficient spoiling can result in inaccurate T<sub>1</sub> estimates of up to 30% relative to inversion recovery estimated values (Stikov et al. 2015). VFA T<sub>1</sub> map accuracy and precision is also strongly dependent on the quality of the measured B<sub>1</sub> map (Lee et al. 2017), which can vary substantially between implementations (Boudreau et al. 2017). Modern rapid B<sub>1</sub> mapping pulse sequences are not as widely available as VFA, resulting in some groups attempting alternative ways of removing the bias from the T<sub>1</sub> maps like generating an artificial B<sub>1</sub> map through the use of image processing techniques (Liberman et al. 2014) or omitting B<sub>1</sub> correction altogether (Yuan et al. 2012). The latter is not recommended, because most MRI scanners have default pulse sequences that, with careful protocol settings, can provide B<sub>1</sub> maps of sufficient quality very rapidly (Boudreau et al. 2017; Wang et al. 2005; Samson et al. 2006).
</p>

<p style="text-align:justify;">
Despite some drawbacks, VFA is still one of the most widely used T<sub>1</sub> mapping methods in research. Its rapid acquisition time, rapid image processing time, and widespread availability makes it a great candidate for use in other quantitative imaging acquisition protocols like quantitative magnetization transfer imaging (Yarnykh 2002; Cercignani et al. 2005) and dynamic contrast enhanced imaging (Sung et al. 2013; Li et al. 2018).
</p>

