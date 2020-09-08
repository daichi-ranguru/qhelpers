# SCSS Magic

## Arrow on top of div

```HTML
    <div class="anyParentWithRelativePosition">
        Any other content
        <div class="pin"></div>
    </div>
```


```SCSS
    .anyParentWithRelativePosition {
        .pin {
            background: transparent;
            bottom: 0; //will be placed at the bottom of its parent
            transform: translate(-50%, 50%) rotate(45deg);
            left: 50%;
            position: absolute;
            border-radius: 4px;
            width: 23px;
            height: 23px;
            overflow: hidden;

            &::after {
                    content: "";
                    position: absolute;
                    width: 100%;
                    height: 100%;
                    top: 0;
                    background: white;
                    transform: translateX(53%) translateY(53%) rotate(-45deg) scale(1.5);
            }
        }
    }
```

## Image not sharp enough? I got your back!

```SCSS
    image-rendering: pixelated;
```