<template>
  <div>
    <div class="cart-page">
      <h1>Cart</h1>
    </div>
    <div class="displ">
      <NavBar />
      <div class="disa">
        <div class="displays">
          <div class="linem">
            <div class="left-side">
              <div class="profile">
                <div class="profi">
                  <img
                    src="https://i.postimg.cc/ZKZpFGGf/a2fa542767141c084b8785205e24d775.jpg"
                    alt=""
                  />
                </div>
                <div class="descrip">
                  <div class="descript">heading</div>
                  <div class="descripture">
                    <p>
                      Lorem ipsum dolor sit amet consectetur adipisicing elit.
                      Inventore rem hic natus pariatur reiciendis cupiditate
                      sapiente! Modi sunt recusandae odit possimus asperiores
                      tempore? Laudantium sint eveniet porro, suscipit adipisci
                      non?
                    </p>
                  </div>
                  <div class="quan">
                    <p>
                      Quantity
                      <span class="righ">Delete</span>
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <div id="entry">
              <div class="leftSide">
                <div class="profile">
                  <div class="profi">
                    <img
                      src="https://i.postimg.cc/ZKZpFGGf/a2fa542767141c084b8785205e24d775.jpg"
                      alt=""
                    />
                  </div>
                  <div class="descrip">
                    <div class="descript">heading</div>
                    <div class="descripture">
                      <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Inventore rem hic natus pariatur reiciendis cupiditate
                        sapiente! Modi sunt recusandae odit possimus asperiores
                        tempore? Laudantium sint eveniet porro, suscipit
                        adipisci non?
                      </p>
                    </div>
                    <div class="quan">
                      <p>
                        Quantity
                        <span class="righ">Delete</span>
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="row2">
              <div class="col-md-auto c2">
                <div class="contai">
                  <div class="para">
                    <div class="desc">Sub-Total</div>
                    <div class="total">
                      <h5>Total</h5>
                    </div>
                    <div class="add">
                      <ul>
                        <li>
                          Sub-Total
                          <span class="right"> R1232</span>
                        </li>

                        <li>
                          Shipping Price
                          <span class="right"> R1232</span>
                        </li>
                      </ul>
                      <ul>
                        <li>
                          Delivery
                          <span class="right">
                            <button
                              type="button"
                              data-bs-toggle="modal"
                              data-bs-target="#exampleModal"
                            >
                              <ion-icon
                                name="information-circle-outline"
                              ></ion-icon></button
                          ></span>
                        </li>
                      </ul>
                    </div>
                    <div class="accepted-card">
                      <img
                        class="acc-car"
                        src="https://i.postimg.cc/MH0PCqNX/Untitled.png"
                        alt=""
                      />
                      <img
                        class="acc-car"
                        src="https://i.postimg.cc/3NQffdLP/Pay-Pal-Logo-500x281.png"
                        alt=""
                      />
                      <img
                        class="acc-car"
                        src="https://i.postimg.cc/2jnKb7ym/Mastercard-Symbol.jpg"
                        alt=""
                      />
                      <img
                        class="acc-car"
                        src="https://i.postimg.cc/W3kf7M7G/American-Express-Logo-700x394.png"
                        alt=""
                      />
                    </div>
                  </div>
                </div>
                <div class="checkout">
                  <button type="submit" class="btn btn-success">
                    Proceed to checkout
                  </button>
                </div>
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

.cart-page {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 4rem;
}
.disa {
  border-radius: 15px;
  max-height: 100%;
  width: 80%;
  height: 35rem;
  /* margin-top: 2rem; */
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

.descrip {
  width: 50%;
  height: 80%;
  margin-top: 30px;
  padding-right: 5px;
  float: right;
  display: inline-block;
  justify-content: center;
  align-items: center;
}
.profi {
  width: 50%;
  height: 80%;
  margin-top: 30px;
  padding-right: 5px;
  float: left;
}

.descript {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 20px;
}
.descripture {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-top: 1rem;
  margin-bottom: 1rem;
  max-height: 100%;
}
.profile {
  border-radius: 15px;
  border: 3px solid black;
  max-height: 100%;
  width: 35rem;
  height: 25rem;
}
.profi img {
  border-radius: 5px;
  max-height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  float: left;
  padding-left: 5px;
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

.desc {
  display: flex;
  justify-content: center;
  align-content: center;
  font-size: 25px;
}
.total {
  display: flex;
  justify-content: center;
  align-content: center;
  color: red;
}

.total h5 {
  font-size: 35px;
}

.row2 {
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
  max-height: 100%;
  width: 50%;
  height: 35rem;
  float: right;
}
.displ {
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
#entry {
  display: none;
}
.add ul li {
  text-decoration: none;
}

.add {
  border-bottom: 1px solid rgba(63, 63, 63, 0.493);
}

.right {
  float: right;
  margin-right: 2rem;
}
.checkout {
  float: right;
}

.right button {
  background: none;
  border: none;
}

.total {
  /* margin: 1rem; */
  margin-left: 1rem;
  margin-right: 1rem;
  border-bottom: 1px solid rgba(63, 63, 63, 0.493);
}

.right ion-icon {
  width: 30px;
  height: 30px;
}

.contai {
  height: 18rem;
  max-width: 100%;
}

.para {
  border: 3px solid black;
}

.accepted-card {
  display: flex;
  justify-content: center;
  align-items: center;
}

.accepted-card img {
  width: 90px;
  margin-top: 1rem;
  margin-bottom: 1rem;
  height: 2rem;
}

.acc-car {
  border: 1px solid black;
  border-radius: 5px;
  background-color: white;
  margin-left: 5px;
}
.righ {
  float: right;
}
@media screen and (max-width: 650px) {
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  .disa {
    display: flex;
    justify-content: center;
    align-content: center;
    height: 20rem;
    width: 15rem;
  }
  .displays {
    display: flex;
    justify-content: center;
    align-content: center;
    max-width: 100%;
    width: 100%;
  }
  .leftSide img {
    width: 8rem;
    height: 13rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .left-side {
    width: 150px;
    height: 300px;
    max-height: 100%;
    display: none;
  }

  .displ {
    display: inline-block;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    max-height: 100%;
    margin-left: 50px;
  }

  #entry {
    display: flex;
    justify-content: center;
    align-items: center;
    visibility: visible;
    margin-top: 3rem;
    width: 50%;
    max-width: 100%;
  }

  .informations {
    width: 20rem;
  }

  .passw {
    float: right;
  }
  .leftSide {
    border-radius: 15px;
    max-height: 100%;
    width: 20rem;
    height: 20rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .tet li {
    margin-bottom: 1rem;
    width: 15rem;
    border-bottom: 2px solid black;
  }

  .other {
    float: right;
  }
  .row2 {
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 15px;
    max-height: 100%;
    width: 20rem;
    height: 35rem;
    margin-left: 1rem;
  }

  .linem {
    display: inline-block;
    justify-content: center;
    align-items: center;
    width: 50%;
  }
  .descripture {
    max-height: 100%;
    max-width: 100%;
    font-size: 10px;
  }
  .profile {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 3rem;
    margin-bottom: 4rem;
  }
  .c2 {
    display: inline-block;
    margin-left: 12rem;
    margin-top: 4rem;
    margin-bottom: 4rem;
    width: 16rem;
  }
}
</style>