--- 
layout: post
title: Translating submit button on ActiveAdmin
date_pt_BR: 02 OUT 2011
---

Hi mate, this is my first english post and it will be about internationalization on active_admin gem.
Currently i am working on a project using Active Admin interface, and i came across with an i18n problem, that is translate the submit buttons.

After google a few i have found an [issue][1] and [another one][2] and both, especially [this comment][3] showed me that the responsible about submit button was the [formtastic][4] and then I just needed to copy content of [formtastic locale file][5] to my locale file and i've got solved that issue.

Take a look below what do you need to do.

<script src="https://gist.github.com/1257776.js?file=pt-br.yml"></script>
<br/>

That's all 

#### DISCLAIMER

Sorry if i made some grammatical mistakes on this text, it is my first english post as i told before. Actually, it is just the first one, I am planning post in english as part of my studies.


Thanks and see ya bro!

[1]: https://github.com/gregbell/active_admin/issues/507
[2]: https://github.com/gregbell/active_admin/issues/349
[3]: https://github.com/gregbell/active_admin/issues/507#issuecomment-2157030
[4]: https://github.com/justinfrench/formtastic
[5]: https://github.com/justinfrench/formtastic/blob/master/lib/locale/en.yml