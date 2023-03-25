<template>
  <div>
    <div class="footer">
      <div class="linkings">
        <ul class="links">
          <li class="nav-item">
            <router-link to="/" class="nav-links">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-links" to="/about">About</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-links" to="/cart">Cart</router-link>
          </li>
        </ul>
        <ul class="links2">
          <li class="nav-item">
            <router-link class="nav-links" to="/admin">Admin</router-link>
          </li>
          <li class="nav-item">
            <router-link to="/contact" class="nav-links"
              >Contact Us</router-link
            >
          </li>
          <li class="nav-item">
            <router-link class="nav-links" to="/login"
              >Login/Register</router-link
            >
          </li>
        </ul>
        <form class="d-flex">
          <input
            class="form-control me-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn" type="submit">Search</button>
        </form>
      </div>
    </div>
    <div class="lower">
      <div class="cop">
        <div class="copy">
          <h3>Copyright &copy Lagom 2023</h3>
        </div>
        <div class="socials">
          <a href="https://www.facebook.com/login/" class="facebook">
            <ion-icon name="logo-facebook"></ion-icon>
          </a>
          <a href="http://instagram.com" class="instagram">
            <ion-icon name="logo-instagram"></ion-icon>
          </a>
          <a href="http://linkedin.com" class="linkedin">
            <ion-icon name="logo-linkedin"></ion-icon>
          </a>
          <a href="http://pinterext.com" class="pinterest">
            <ion-icon name="logo-pinterest"></ion-icon>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style>
.footer {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-top: 2px solid black;
  margin-top: 3rem;
}
.footer .linkings .links {
  width: 15rem;
  height: auto;
  max-width: 100%;
}
.lower .cop .cpoy {
  width: 15rem;
  height: auto;
  max-width: 100%;
}
.links2 {
  width: 15rem;
}
.links2 .d-flex {
  max-width: 100%;
  width: 15rem;
  /* padding: 0 10px; */
}
.d-flex {
  margin-bottom: 1rem;
}
.cop {
  /* float: right; */
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
  width: 1280px;
  max-width: 95%;
  margin: 0 auto;
}
.copy {
  margin-top: 1rem;
  margin-bottom: 1rem;
  color: grey;
}
.linkings {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
  width: 1280px;
  max-width: 95%;
  margin: 0 auto;
}
.lower {
  background-color: black;
  /* margin-top: 2rem; */
}
.socials {
  color: white;
  font-size: 25px;
  margin-top: 1rem;
  margin-bottom: 1rem;
}
.btn {
  color: black;
}

.socials a {
  background: transparent;
  color: white;
  border: transparent;
  padding-left: 1rem;
}

.facebook:hover {
  color: rgb(68, 99, 238);
}
.instagram:hover {
  color: rgb(179, 84, 136);
}
.linkedin:hover {
  color: rgb(68, 99, 238);
}
.pinterest:hover {
  color: red;
}
</style>