# to_be_god
just a record for using emacs.

成为神的必经之路就是使用emacs，那么2016年的某一天，我下一个从[官网](https://www.gnu.org/software/emacs/)上下了一只emacs

### next1
接着发现了一年成神的文章:[mastering-emacs-in-one-year-guide](https://github.com/redguardtoo/mastering-emacs-in-one-year-guide)，我大概浏览了一遍，大概真的可行吧。

便先按照文章里的说明，看了官方的基本教程，学了几个快捷键。然后clone了[Purcell的".emacs.d](https://github.com/purcell/emacs.d)，后来在shell里输入了下emacs，然后就跟readme里面说的一样开始下载，等到全部下载好之后，发现emacs就从白色变成了黄拉拉的颜色。

ok，我真的不太喜欢这个theme，于是就谷歌了一下theme，发现了[purcell还有一个theme仓库](https://github.com/purcell/color-theme-sanityinc-tomorrow)，然后很喜欢那种blue的感觉，就...

看了一下他的[.emacs.d/lisp/init-themes.el](https://github.com/purcell/emacs.d/blob/master/lisp/init-themes.el)发现他写了几个defun么，随便按照英文意思大概了解了他的意思，便在自己的emacs里输入了```M-x dark```果然变成了黑色皮肤，而在开头看见他的```(require-package 'color-theme-sanityinc-tomorrow)```所以就按照readme，在lisp里面创建了一个init-local.el，然后写了一个方法


```lisp
;; emacs blue 主题
(defun blue ()
  "Activate a blue color theme."
  (interactive)
  (color-theme-sanityinc-tomorrow-blue))

```
之后```M-x blue```来使用blue主题，我的terminal也是有点小透明，是否我的emacs也可以有点小透明？便找到了[alpha_value.el](https://gist.github.com/cosmo0920/3800026)，cp到init-local.el中之后，执行了下C-x a，然后就80%透明了，然后修改了一下，90%可以接受。

###next2
* 虽然站在了[purcell](https://github.com/purcell/emacs.d)的肩膀上面，但是始终只是开始，接下来就是让自己习惯快捷键这种uncomfortable，于是就把自己的phpstorm编辑器的这种快捷键keymap也都设置成了emacs（有点反人类，不好的地方就是不能使用到emacs上的那种插件，但重要原因可能是一时间不太习惯emacs这种暴力的模式吧，况且手头上的项目仍需开发）
* 学习一些elisp，[elisp简明教程🙈](http://smacs.github.io/elisp/)
