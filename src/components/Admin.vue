<template>
  <div class="body" v-if="product">
    <div v-if="user">
      <NavBar />
      <div>
        <div class="container ">
          <div class="row table-container">
            <div class="col-12">
              <h1>Users</h1>
              <button
                type="button"
                class="btn btn-success add-btn"
                data-bs-toggle="modal"
                data-bs-target="#addUserModal"
              >
                Add
              </button>
            </div>
            <div class="col">
              <table class="table is-striped is-bordered mt-2 is-fullwidth array-lists">
                <thead>
                  <tr>
                    <th>#</th>
                    <th>FirstName</th>
                    <th>LastName</th>
                    <th>Email</th>
                    <th>Image</th>
                    <th>Edit/Delete</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="item in user" :key="item.userID" class="bord">
                    <td>{{ item.userID }}</td>
                    <td>{{ item.firstName }}</td>
                    <td>{{ item.lastName }}</td>
                    <td>{{ item.emailAdd }}</td>
                    <td><img class="tableImg" :src="item.imgPro" alt="" /></td>
                    <td>
                      <button
                        type="button"
                        class="btn bton"
                        data-bs-toggle="modal"
                        data-bs-target="#editUserModal"
                        id="edit-row"
                      >
                        Edit
                      </button>
                      <button
                        type="button"
                        class="btn btton"
                        data-bs-toggle="modal"
                        data-bs-target="#exampleModal"
                        id="delete-row"
                      >
                        Delete
                      </button>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
          <div class="row table-container">
            <div class="col-12">
              <h1>Products</h1>
              <button
                type="button"
                class="btn btn-success add-btn"
                data-bs-toggle="modal"
                data-bs-target="#addProductModal"
              >
                Add
              </button>
            </div>
            <div class="col">
              <table class="table is-striped is-bordered mt-2 is-fullwidth array-listsarray-lists"  @submit="deleteProduct">
                <thead>
                  <tr>
                    <th>#</th>
                    <th>Product Name</th>
                    <th>Price</th>
                    <th>Category</th>
                    <th>Quantity</th>
                    <th>Image</th>
                    <th>Edit/Delete</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="item in product" :key="item.id" class="bord">
                    <td>{{ item.id }}</td>
                    <td>{{ item.prodName }}</td>
                    <td>R {{ item.price }}</td>
                    <td>{{ item.category }}</td>
                    <td>{{ item.quantity }}</td>
                    <td><img class="tableImg" :src="item.image" alt="" /></td>
                    <td>
                      
                      <button
                        type="button"
                        class="btn bton"
                        data-bs-toggle="modal"
                        data-bs-target="#editProductModal"
                        id="edit-row"
                      >
                        Edit
                      </button>
                      <button
                        type="submit"
                        class="btn btton"
                        @click="($event) => deleteProduct()"
                        id="delete-row"
                      >
                        Delete
                      </button>
                    </td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
      <Delete />
    </div>
    <div v-else>
      <Spinner />
    </div>
  </div>
  <div v-else>
    <Spinner />
  </div>
</template>

<script>
import axios from "axios";
import NavBar from "../components/NavBar.vue";
import Spinner from "../components/Spinner.vue";
import Delete from "../components/DeleteProduct.vue";
import store from "@/store";
export default {
  name: "admin-Comp",
  components: {
    NavBar,
    Spinner,
    Delete,
    store
  },
  data() {
    return {
      product: [],
      user: [],
    };
  },
  created() {
    this.getProducts();
    this.getUsers();
    this.deleteProduct();
  },
  
  methods: {
    async getProducts() {
      try {
        const response = await axios.get(
          "https://lagom-project.onrender.com/products"
        );
        this.product = response.data.results;
        console.log(response);
      } catch (err) {
        console.log(err);
      }
    },
    async getUsers() {
      try {
        const response = await axios.get(
          "https://lagom-project.onrender.com/users"
        );
        this.user = response.data.results;
        console.log(response);
      } catch (err) {
        console.log(err);
      }
    },
    async deleteProduct() {
      try {
        await axios.delete(`https://lagom-project.onrender.com/products/${id}`);
        this.deleteProduct();
      } catch (err) {
        console.log(err);
      }
    },
  },
};
</script>

<style scoped>
.add-btn {
  float: right;
}
tbody button {
  width: 5rem;
  margin-top: 4px;
}
.tableImg {
  height: 50px;
  width: 100px;
  object-fit: contain;
}
.row {
  width: 80rem;
  max-width: 100%;
  /* text-align: center; */
}
.add-btn {
  float: right;
}
.bton {
  background: transparent;
  border: transparent;
}
.btton {
  background: transparent;
  border: transparent;
}
.bton:hover {
  background: blue;
  color: white;
  border: 1px solid black;
}
.btton:hover {
  background: red;
  color: white;
  border: 1px solid black;
}
.table {
  border-bottom: 1px solid black;
  justify-content: center;
  align-items: center;
  border-collapse: collapse;
}
.container {
  margin-top: 5rem;
  text-align: center;
}
@media screen and (max-width: 650px) {
  .body {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 80%;
    max-width: 100%;
  }
  .container {
    display: inline-block;
    justify-content: center;
    align-content: center;
    width: 15rem;
    margin-left: 5rem;
  }
  .bord {
    border: 2px solid black;
  }
  tbody {
    margin-bottom: 2rem;
  }
  thead {
    display: none;
  }
  tbody td {
    /* flex-wrap: wrap; */
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>