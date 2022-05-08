<template>
    <div class="product-list">
        <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4">
            <h2 class="display-4">User Management</h2>
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
                        <tr>
                            <th scope="row">1</th>
                            <td>test</td>
                            <td>test</td>
                            <td>test</td>
                            <td>test</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</template>