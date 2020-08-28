# Themed switches

```
@mixin theme-custom-switch($color) {
    .custom-control-input:checked ~ .custom-control-label {
        &::before {
            background-color: $color;
            border-color: $color;
        }
    }
}

@each $label, $color in $theme-colors {
    .custom-switch-#{$label} {
        @extend .custom-switch;
        @include theme-custom-switch($color);
    }
}
```