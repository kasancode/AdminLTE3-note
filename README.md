# AdminLTE 3.0 メモ

## Navbar

ver2. とは異なり、ロゴは `sidebar` に入った。

`navbar`にロゴを入れるときは、特別な書き方が必要。

```css
nav.main-header .navbar .navbar-expand .navbar-white .navbar-light
 /* logo */
 a.navbar-brand
  img.brand-image .img-circle .elevation-3 /*style="opacity: .8"*/
   span.brand-text
 ul.navbar-nav
  /* basic */
  li.nav-item
   a.nav-link
    i
  /* dropdown */
  li.nav-item
   a.nav-link .dropdown-toggle /*data-toggle="dropdown"*/
   div.dropdown-menu
    a.dropdown-item
    div.dropdown-divider
 /* form */
 form.form-inline .ml-3
  div.input-group .input-group-sm
   input.form-control .form-control-navbar
   div.input-group-append
    button.btn .btn-navbar
```



## Sidebar

ロゴの入れ方は `nav-bar`と似ているが、`a` の`class` が異なる。

```css
aside.main-sidebar .sidebar-dark-primary .elevation-4
 /* logo */
 a.brand-link
  img.brand-image .img-circle .elevation-3 /*style="opacity: .8"*/
   span.brand-text
 /* sidebar */
 div.sidebar
  /* user panel */
  div.user-panel .mt-3 .pb-3 .mb-3 .d-flex
   div.image
    img.img-circle .elevation-2
   div.info
    a.d-block
  nav.mt-2
   ul.nav .nav-pills .nav-sidebar .flex-column /*data-widget="treeview" role="menu"*/
    li.nav-item .has-treeview .menu-oepn
     a.nav-link .active
      i.nav-icon
      p
       i.right .fas .fa-angle-left
     ul.nav .nav-treeview
      li.nav-item
       a.nav-link .active
        i.nav-icon
        p
```

IE だとパカパカするので、

```css
body.hold-transition
```

を入れればよい。実行時は、最初のアニメーションを抑制した後で消える模様。

## 基本

```
html
 head
  body.sidebar-mini .layout-fixed

```

## カード

`.box` が `.card` になった。

```css
div.row
 section.col .connectedSortable
  div.card
   div.card-header
    div.card-title
     h3
      i
    div.card-tools
     ul.nav .nav-pills .ml-auto
      li.nav-item
       a.nav-link .active
   div.card-body
    div.tab-content .p-0

```

`Bootstrap` も `.panel` が `.card` になった。



# Bootstrap 4

- `.float-right` は `.col` の中でしか使えない。`.row` 内もNG ?
- `.form-inline` の中の `input` の幅は自動的に小さくなる。`.col`でコントロールできない ?
- `.row` は幅いっぱいまで使う効果はあまりない。`.container-fluid` か `.col-12` を使ったほうが良い。マージンをリセットする効果は `.no-gutters` になった。
- 下手に`.col` に `.m*` で横方向のマージン調整をすると幅12に収まらなくなる?



