# bootstrap

# 常用class
1. label-control
2. pull-right
3. col-xs-offset-2
4. form-inline
5. form-horizontal
6. form-control
7. help-block
8. center-block
9. role="presentation"
10. class="divider"
11. btn-group, btn-toolbar, role
12. input-group-addon, input-group-btn
13. icon
14. br
15. nav nav-tabs
16. data-toggle, data-target, icon-bar
17. &larr;
18. badge
19. page-header
20. media meida-body
21. list-group, list-group-item, list-group-item-text/heading
22. panel
(这个属性超级有用)

## 感想
div, ui, form这些其实只是一个容器，定义了容器里的一些全局属性

容器和一个具体的元素，如p, span, label间的区别

各个元素到底是块级元素，还是行级元素

## code
```language
<div class="alert alert-warning alert-dismissable">
   <button type="button" class="close" data-dismiss="alert"
      aria-hidden="true">
      &times;
</button>
   Warning ! Dont submit this.
</div>
```
```language
<span class="caret"></span>
```

```
<p>Tabs Example</p>
<ul class="nav nav-tabs">
   <li class="active"><a href="#">Home</a></li>
   <li><a href="#">SVN</a></li>
   <li><a href="#">iOS</a></li>
   <li><a href="#">VB.Net</a></li>
   <li><a href="#">Java</a></li>
   <li><a href="#">PHP</a></li>
</ul>
```
```
<button type="button" class="btn btn-default btn-xs">
  <span class="glyphicon glyphicon-user"></span> User
</button>
```
```html
<div class="checkbox">
   <label><input type="checkbox" value="">Option 1</label>
</div>
<div class="checkbox">
   <label><input type="checkbox" value="">Option 2</label>
</div>
<div class="radio">
   <label>
      <input type="radio" name="optionsRadios" id="optionsRadios1"
         value="option1" checked> Option 1
   </label>
</div>
<div class="radio">
   <label>
      <input type="radio" name="optionsRadios" id="optionsRadios2"
         value="option2">
         Option 2 - selecting it will deselect option 1
   </label>
</div>
<label for="name">Example of Inline Checkbox and radio button </label>
<div>
   <label class="checkbox-inline">
      <input type="checkbox" id="inlineCheckbox1" value="option1"> Option 1
   </label>
   <label class="checkbox-inline">
```

```html
<select multiple class="form-control">
         <option>1</option>
         <option>2</option>
         <option>3</option>
         <option>4</option>
         <option>5</option>
      </select>
```

```html
<label class="col-sm-2 control-label">Email</label>
    <div class="col-sm-10">
      <p class="form-control-static">email@example.com</p>
    </div>
```