<template>
    <div class="product-list">
        <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4">
            <h2 class="display-4">Product Management</h2>
            <p><router-link to="/product/create">Create</router-link></p>
        </div>

        <div class="container">
            <div class="card-deck mb-3 text-center">
                <table class="table table-bordered">
                    <thead>
                        <tr>
                            <th scope="col">#</th>
                            <th scope="col">Product Name</th>
                            <th scope="col">Price</th>
                            <th scope="col">Handle</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr :key="index" v-for="(product, index) in products">
                            <th scope="row">{{ index + 1 }}</th>
                            <td>{{ product.name }}</td>
                            <td>{{ product.price }}</td>
                            <td>{{ product.description }}</td>
                            <td>
                                <router-link :to="{ name: 'product.edit', params: {id: product.id} }"> 
                                    <button class="btn btn-primary">Edit</button> 
                                </router-link>                               
                                <button class="btn btn-danger" @click="onDelete(product.id)">Delete</button>
                            </td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'productForm',
    data () {
        return {
            products: {

            }
        }
    },
    created () {
        this.getAllProducts()
    },
    methods: {
        getAllProducts() {
            this.$request.get('http://localhost:8000/api/products').then(res => {
                this.products = res.data
            });
        },
        onDelete(productId) {
            this.$swal.fire({
            title: 'Do you want to delete',
            showDenyButton: false,
            showCancelButton: true,
            confirmButtonText: 'Ok',
            }).then((result) => {
                if (result.isConfirmed) {
                    this.$request.delete(`http://localhost:8000/api/products/${productId}`).then(res => {
                    if (res.data.success) {
                        this.$swal.fire('Deleted!', '', 'success')
                        this.getAllProducts()
                    }
                    })
                } else if (result.isDenied) {
                    this.$swal.fire('Changes are not saved', '', 'info')
                }
            })
        }
    }
}
</script>