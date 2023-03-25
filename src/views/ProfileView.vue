<template>
  <div class="disp">
    <NavBar />
    <div class="dis">
      <div class="display">
        <div class="left-side">
          <div class="profile-img">
            <img
              src="https://i.postimg.cc/P5R6CrKR/IMG-20230311-175710-1.jpg"
              alt=""
            />
          </div>
        </div>
        <div class="right-side">
          <div class="info-text">
            <div class="information">
              <div class="text">
                <ul>
                  <li>
                    Full-Name:
                    <span class="right">Abdul-Azeez Kemp</span>
                  </li>
                  <li>
                    Email Address:
                    <span class="right">aakemp786@gmail.com</span>
                  </li>
                  <li>
                    Cell-Number:
                    <span class="right">0827869214</span>
                  </li>
                  <ol class="pass">
                    <button type="submit" class="password">
                      Change Password
                    </button>
                  </ol>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";

export default {
  name: "Profile",
  components: {
    NavBar,
  },
};
</script>

<style >
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.dis {
  border-radius: 15px;
  border: 2px solid black;
  max-height: 100%;
  width: 80%;
  height: 35rem;
  margin-top: 6rem;
}
.left-side {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
  max-height: 100%;
  width: 50%;
  height: 35rem;
  float: left;
}
.profile-img img {
  border-radius: 15px;
  border: 3px solid black;
  max-height: 100%;
  width: 25rem;
  height: 25rem;
}
.info-text {
  border-radius: 15px;
  max-height: 100%;
  width: 30rem;
  height: 25rem;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 5rem;
}
.information {
  border-radius: 15px;
  max-height: 100%;
  width: 30rem;
  height: 18rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.text li {
  margin-bottom: 3rem;
  width: 30rem;
  border-bottom: 3px solid black;
}

.right {
  float: right;
  /* margin-right: 2rem; */
}

.right-side {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
  max-height: 100%;
  width: 50%;
  height: 35rem;
  float: right;
}
.disp {
  display: flex;
  justify-content: center;
  align-items: center;
}

.pass {
  float: right;
}

.password {
  background-color: transparent;
  border: transparent;
  text-decoration: underline;
  color: blue;
}

.password:hover {
  color: rgb(3, 3, 138);
}
/* @media screen and (max-width: 768px) {
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .dis {
    display: flex;
    justify-content: center;
    align-content: center;
  }
  .display {
    display: inline-block;
    justify-content: center;
    align-content: center;
  }
  .profile-img img {
    width: 14rem;
    height: 18rem;
    border-radius: 5px;
    border: 2px solid black;
  }
  .left-side {
    width: 150px;
    height: 300px;
    max-height: 100%;
  }
  .right-side {
    width: 150px;
    height: 300px;
    max-height: 100%;
  }
  .disp {
    display: block;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    max-height: 100%;
  }
  .card {
    width: 22rem;
    margin-top: 2rem;
    margin-bottom: 2rem;
  }
  .heading {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 5rem;
  }
  .heading h1 {
    font-size: 20px;
    text-align: center;
  }

  .desc1 {
    margin-bottom: 3rem;
  }

  .smaller img {
    width: 22rem;
    height: 18rem;
    border-radius: 5px;
    border: 2px solid black;
  }
} */
@media screen and (max-width: 650px) {
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .dis {
    display: inline-block;
    justify-content: center;
    align-content: center;
    height: 20rem;
    width: 15rem;
  }
  .display {
    display: flex;
    justify-content: center;
    align-content: center;
    max-width: 100%;
    width: 100%;
  }
  .profile-img img {
    width: 14rem;
    height: 18rem;
    border-radius: 5px;
    border: 2px solid black;
  }
  .left-side {
    width: 150px;
    height: 300px;
    max-height: 100%;
  }
  .right-side {
    width: 50px;
    height: 30px;
    max-height: 100%;
    display: none;
  }
  .disp {
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    max-height: 100%;
  }
  .card {
    width: 14rem;
    margin-top: 2rem;
    margin-bottom: 2rem;
  }
  .heading {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 5rem;
  }
  .heading h1 {
    font-size: 20px;
    text-align: center;
  }

}
</style>