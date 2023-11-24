<template>
  <footer class="footer">
    <div class="footer__center">
      <address class="footer__center__address">
        <div class="footer__center__address__copyright">Copyright (c) 2023</div>
        <div class="footer__center__address__divisor"></div>
        <a
          class="footer__center__address__email"
          href="mailto:clarifionsupport@clarifion.com"
          >clarifionsupport@clarifion.com</a
        >
      </address>
      <div class="footer__center__right">
        <div class="footer__center__right__icon">
          <img
            src="../assets/lock.svg"
            alt="lock"
            class="footer__center__right__icon__img"
          />
        </div>
        <div class="footer__center__right__text">
          Secure 256-bit SSL encryption.
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
.footer {
  display: flex;
  padding-top: 24px;
  padding-bottom: 24px;
  padding-left: 127px;
  padding-right: 127px;
  justify-content: center;
  background-color: #252f3d;
}

.footer__center {
  display: flex;
  max-width: 1666px;
  width: 100%;
  justify-content: space-between;
}

.footer__center__address {
  display: flex;
  gap: 16px;
  align-items: center;
}

.footer__center__address__copyright {
  font-family: "Manrope";
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%; /* 22.4px */
  text-transform: capitalize;
  color: #fff;
}

.footer__center__address__divisor {
  background-color: #fff;
  width: 1px;
  height: 24px;
}

.footer__center__address__email {
  color: #fff;
  font-family: Manrope;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%; /* 22.4px */
  text-transform: lowercase;
  text-decoration: none;
  transition-duration: 0.3s;
}

.footer__center__address__email:hover {
  color: #2c7ef8;
}

.footer__center__address__email:visited {
  color: #fff;
}

.footer__center__right {
  display: flex;
  gap: 16px;
  align-items: center;
}

.footer__center__right__text {
  color: #fff;
  text-align: center;
  font-family: Manrope;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 150%; /* 24px */
  text-transform: capitalize;
}

@media only screen and (max-width: 940px) {
  .footer {
    padding: 20px;
  }
  .footer__center {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 27.5px;
  }

  .footer__center__address {
    gap: 12px;
  }
  .footer__center__address__divisor {
    height: 14px;
  }

  .footer__center__address__copyright {
    color: #fff;
    font-family: Manrope;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 140%; /* 16.8px */
    text-transform: capitalize;
  }

  .footer__center__address__email {
    color: #fff;
    font-family: Manrope;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 140%; /* 16.8px */
  }
  .footer__center__right__text {
    color: #fff;
    font-family: Manrope;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 140%; /* 16.8px */
  }
  .footer__center__right {
    align-items: self-start;
  }
  .footer__center__right__icon {
    width: 13px;
    height: 13px;
  }

  .footer__center__right__icon__img {
    width: 13px;
    height: 13px;
  }
}
</style>
