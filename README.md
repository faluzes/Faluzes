# Faluzes » Anouar Aissaoui

[![Faluzes](https://cdn.statically.io/img/faluzes.me/f=auto/wp-content/uploads/2021/12/cropped-Faluzes-logo.png)](https://faluzes.me/)

## Anouar Aissaoui

Hi, I'm `Anouar Aissaoui`, a Digital Marketing expert With 4+ years experience. I have helped brands manage their digital presence through SEO

<div class="social-icons">
  <a class="social-icon social-icon--codepen">
    <i class="fa fa-codepen"></i>
    <div class="tooltip">Codepen</div>
  </a>
  <a class="social-icon social-icon--github">
    <i class="fa fa-github"></i>
    <div class="tooltip">Github</div>
  </a>
  <a class="social-icon social-icon--twitter">
    <i class="fa fa-twitter"></i>
    <div class="tooltip">Twitter</div>
  </a>
  <a class="social-icon social-icon--dribbble">
    <i class="fa fa-dribbble"></i>
    <div class="tooltip">Dribbble</div>
  </a>
  <a class="social-icon social-icon--instagram">
    <i class="fa fa-instagram"></i>
    <div class="tooltip">Instagram</div>
  </a>
  <a class="social-icon social-icon--linkedin">
    <i class="fa fa-linkedin"></i>
    <div class="tooltip">LinkedIn</div>
  </a>
  <a class="social-icon social-icon--facebook">
    <i class="fa fa-facebook"></i>
    <div class="tooltip">Facebook</div>
  </a>
</div>











/* Demo */
body {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }
  
  /* Color Variables */
  $color-codepen: #000;
  $color-github: #4284c0;
  $color-twitter: #2b97f1;
  $color-dribbble: #ef5a92;
  $color-instagram: #527fa6;
  $color-linkedin: #006599;
  $color-facebook: #3b5a9b;
  
  /* Social Icon Mixin */
  @mixin social-icon($color) {
    background: $color;
    color: #fff;
  
    .tooltip {
      background: $color;
      color: currentColor;
  
      &:after {
        border-top-color: $color;
      }
    }
  }
  
  /* Social Icons */
  .social-icons {
    display: flex;
  }
  
  .social-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    width: 80px;
    height: 80px;
    margin: 0 0.5rem;
    border-radius: 50%;
    cursor: pointer;
    font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
    font-size: 2.5rem;
    text-decoration: none;
    transition: all 0.15s ease;
  
    &:hover {
      color: #fff;
  
      .tooltip {
        visibility: visible;
        opacity: 1;
        transform: translate(-50%, -150%);
      }
    }
      
    &:active {
      box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.5) inset;
    }
    
    &--linkedin { @include social-icon($color-linkedin); }
    &--twitter { @include social-icon($color-twitter); }
    &--codepen { @include social-icon($color-codepen); }
    &--facebook { @include social-icon($color-facebook); }
    &--instagram { @include social-icon($color-instagram); }
    &--dribbble { @include social-icon($color-dribbble); }
    &--github { @include social-icon($color-github); }
    
    i {
      position: relative;
      top: 1px;
    }
  }
  
  /* Tooltips */
  .tooltip {
    display: block;
    position: absolute;
    top: 0;
    left: 50%;
    padding: 0.8rem 1rem;
    border-radius: 40px;
    font-size: 0.8rem;
    font-weight: bold;
    opacity: 0;
    pointer-events: none;
    text-transform: uppercase;
    transform: translate(-50%, -100%);
    transition: all 0.3s ease;
    z-index: 1;
    
    &:after {
      display: block;
      position: absolute;
      bottom: 1px;
      left: 50%;
      width: 0;
      height: 0;
      content: "";
      border: solid;
      border-width: 10px 10px 0 10px;
      border-color: transparent;
      transform: translate(-50%, 100%);
    }
  }