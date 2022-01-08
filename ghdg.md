HTML

```html
<div class="m-text">
  <label class="m-text__label" for="ip-name-id">First Name</label>
  <input class="m-text__ip" id="ip-name-id" />
</div>

<div class="m-text m-text--success">
  <label class="m-text__label" for="ip-name-id2">First Name</label>
  <input class="m-text__ip" id="ip-name-id2" />
</div>

<div class="m-text m-text--error">
  <label class="m-text__label" for="ip-name-id2">First Name</label>
  <input class="m-text__ip" id="ip-name-id2" />
</div>
```

```scss
.m-text {
  $classname: m-text;
  
  &__label {
    color: darkgray;
    display: block;
  }
  
  &__ip {
    padding: 5px 10px;
    border: 1px solid lightgray;
  }
  
  &::after {
    content: '';
    display: none;
  }
  
  // .m-text--success
  &--success {
    
    // .m-text__label
    .#{$classname}__label {
      color: green;
    }
    
    .#{$classname}__ip {
      border: 1px solid green;
    }
    
    &::after {
      content: 'success-icon';
      display: block;
    }
  }
  
  &--error {
    .#{$classname}__label {
      color: red;
    }
    
    .#{$classname}__ip {
      border: 1px solid red;
    }
    
    &::after {
      content: 'error-icon';
      display: block;
    }
  }
}
```