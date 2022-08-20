<template>
  <main class="home">
    <nav>
      <div class="lang">
        <img src="@/assets/img/icon.svg" alt="">
        <div class="selectors">
          <Link class="ua" text="UA"/>
          <Link class="ru" text="RU"/>
        </div>
      </div>
      <div class="logo">
        <img src="@/assets/img/Logo.svg" alt="">
      </div>
      <div class="burger">
        <!-- Тут мав бути бургер, але не склалось -->
      </div>
    </nav>
    <div class="runing-lines">
      <div class="line">
        <span>full-cycle event ageny full-cycle event agency full-cycle event agency</span>
        <span>full-cycle event ageny full-cycle event agency full-cycle event agency</span>
      </div>
      <div class="line">
        <span>full-cycle event ageny full-cycle event agency full-cycle event agency</span>
        <span>full-cycle event ageny full-cycle event agency full-cycle event agency</span>
      </div>
    </div>
    <div class="content">
      <div class="circle">
        <span></span>
        <router-link :to="{ name: '', params: {} }">
          <img src="@/assets/img/button.svg" alt="">
        </router-link>
      </div>
      <div class="title">
        <h1>full-cycle<br>event agency</h1>
      </div>
    </div>
    <Link class="bottom" text="who?"/>
    <Link class="left" text="where?"/>
    <Link class="right" text="what?"/>
  </main>
</template>

<script>
import Link from '@/components/Link.vue';

export default {
  name: 'Home',
  components: {
    Link,
  }
}
</script>

<style lang="scss" scoped>
  .home {
    nav {
      width: 100%;
      position: fixed;
      display: flex;
      justify-content: space-between;
      padding: 24px;
      align-items: center;

      .lang {
        height: 38px;
        width: 38px;
        border-radius: 50%;
        border: 1px solid #FFFFFF1E;
        cursor: pointer;

        &:hover {
          .selectors {
            opacity: 1;
          }
        }

        img {
          display: block;
          margin: 0 auto;
          width: 15px;
          padding-top: 12px;
        }

        .selectors {
          opacity: 0;
          transition: .3s all;

          .ua {
            left: 76px;
            top: 40px;
          }

          .ru {
            left: 126px;
            top: 40px;
          }
        }
      }

      .logo {
        img {
          height: 46px;

          @media screen and (max-width: $xl) {
            height: 41px;
          }

          @media screen and (max-width: $lg) {
            height: 36px;
          }

          @media screen and (max-width: $md) {
            height: 31px;
          }

          @media screen and (max-width: $sm) {
            height: 26px;
          }
        }
      }

      .burger {
        height: 34px;
        width: 22px;
        cursor: pointer;
        position: relative;

        &::before {
          content: '';
          position: absolute;
          width: 22px;
          height: 1px;
          background-color: $black;
          top: 12px;
          right: 0;
        }

        &::after {
          content: '';
          position: absolute;
          width: 22px;
          height: 1px;
          background-color: $black;
          bottom: 12px;
          right: 0;
        }
      }
    }

    .runing-lines {
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%) rotate(-30deg);

      @media screen and (max-width: $xl) {
        transform: translate(-50%, -50%) rotate(-33deg);
      }

      @media screen and (max-width: $lg) {
        transform: translate(-50%, -50%) rotate(-37deg);
      }

      @media screen and (max-width: $md) {
        transform: translate(-50%, -50%) rotate(-46deg);
      }

      @media screen and (max-width: $sm) {
        transform: translate(-50%, -50%) rotate(-64deg);
      }

      .line {
        overflow: hidden;
        display: flex;

        span {
          display: block;
          font-style: italic;
          font-weight: 700;
          font-size: 52px;
          line-height: 57px;
          text-transform: uppercase;
          opacity: 0.1;
          width: 100%;
          height: 100%;
          -webkit-text-stroke: 1px $d-gray;
          color: transparent;
          white-space: nowrap;
          animation: 30s slidein infinite linear;

          @media screen and (max-width: $xl) {
            font-size: 46px;
            line-height: 49px;
          }

          @media screen and (max-width: $lg) {
            font-size: 40px;
            line-height: 42px;
          }

          @media screen and (max-width: $md) {
            font-size: 34px;
            line-height: 37px;
          }

          @media screen and (max-width: $sm) {
            font-size: 28px;
            line-height: 31px;
          }
        }

        &:first-of-type {
          margin-bottom: 16px;
          transform: rotate(180deg);

          @media screen and (max-width: $lg) {
            margin-bottom: 12px;
          }

          @media screen and (max-width: $sm) {
            margin-bottom: 8px;
          }
        }
      }

      @keyframes slidein {
        0% {
          transform: translateX(50%);
        }

        100% {
          transform: translateX(-50%);
        }
      }
    }

    .content {
      display: flex;
      height: 100vh;
      width: 100%;
      justify-content: center;
      align-items: center;

      .circle {
        position: relative;

        span {
          display: block;
          border-radius: 50%;
          filter: blur(32px);
          width: 578px;
          height: 578px;
          background-color: $yellow;

          @media screen and (max-width: $xl) {
            width: 507px;
            height: 507px;
            filter: blur(28px);
          }

          @media screen and (max-width: $lg) {
            width: 436px;
            height: 436px;
            filter: blur(24px);
          }

          @media screen and (max-width: $md) {
            width: 365px;
            height: 365px;
            filter: blur(20px);
          }

          @media screen and (max-width: $sm) {
            width: 294px;
            height: 294px;
            filter: blur(16px);
          }
        }

        a {
          position: absolute;
          bottom: 24px;
          right: 24px;

          @media screen and (max-width: $xl) {
            bottom: 14px;
            right: 14px;
          }

          @media screen and (max-width: $lg) {
            bottom: 4px;
            right: 4px;
          }

          @media screen and (max-width: $md) {
            bottom: -6px;
            right: -6px;
          }

          @media screen and (max-width: $sm) {
            bottom: -16px;
            right: -16px;
          }

          img {
            height: 115px;
            animation: 10s rotate_img infinite linear paused;

            &:hover {
              -webkit-animation-play-state: running;
            }

            @media screen and (max-width: $xl) {
              height: 109px;
            }

            @media screen and (max-width: $lg) {
              height: 103px;
            }

            @media screen and (max-width: $md) {
              height: 97px;
            }

            @media screen and (max-width: $sm) {
              height: 91px;
            }
          }

          @keyframes rotate_img {
            0% {
              transform: rotate(0deg);
            }

            100% {
              transform: rotate(360deg);
            }
          }
        }
      }

      .title {
        position: absolute;

        h1 {
          line-height: 90px;
          font-size: 82px;
          font-weight: 700;
          text-transform: uppercase;
          text-align: center;

          @media screen and (max-width: $xl) {
            line-height: 77px;
            font-size: 70px;
          }

          @media screen and (max-width: $lg) {
            line-height: 64px;
            font-size: 58px;
          }

          @media screen and (max-width: $md) {
            line-height: 51px;
            font-size: 46px;
          }

          @media screen and (max-width: $sm) {
            line-height: 38px;
            font-size: 34px;
          }
        }
      }
    }

    .link {
      &.left {
        left: -10px;
        top: 50%;
        transform: translateY(-50%) rotate(-90deg);

        @media screen and (max-width: $lg) {
          left: -14px;
        }

        @media screen and (max-width: $md) {
          left: -18px;
        }

        @media screen and (max-width: $md) {
          display: none;
        }
      }

      &.bottom {
        bottom: 20px;
        transform: translateX(-50%);
        left: 50%;

        @media screen and (max-width: $lg) {
          bottom: 16px;
        }

        @media screen and (max-width: $md) {
          bottom: 12px;
        }

        @media screen and (max-width: $md) {
          display: none;
        }
      }

      &.right {
        right: -10px;
        top: 50%;
        transform: translateY(-50%) rotate(90deg);

        @media screen and (max-width: $lg) {
          right: -8px;
        }

        @media screen and (max-width: $md) {
          display: none;
        }
      }
    }
  }

</style>
