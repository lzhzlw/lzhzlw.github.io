# Zhenhai Liu - AcadHomepage

forked from [RayeRen/acad-homepage.github.io](https://github.com/RayeRen/acad-homepage.github.io) and [Xiaoyang0118/xiaoyang0118.github.io](https://github.com/Xiaoyang0118/xiaoyang0118.github.io)

## Change your avatar from round to square
**_sass/_sidebar.scss**
```
.author__avatar {
  display: table-cell;
  vertical-align: top;
  width: 75px;
  // set width only, for non-square avatars
  height: 75px;

  @include breakpoint($large) {
    display: block;
    width: auto;
    height: auto;
  }

  img {
    max-width: 175px;
    min-width: 75px;
    border-radius: 0%;//50%;

    @include breakpoint($large) {
      padding: 5px;
      border: 1px solid $border-color;
    }
  }
}
```
Change 50% to 0%
