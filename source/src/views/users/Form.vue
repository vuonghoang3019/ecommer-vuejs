<template>
    <div class="product-info">
        <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
            <h3 class="display-5">User Information</h3>
            <p><router-link to="/users">Back</router-link></p>
        </div>

        <div class="container">
            <form>
                <div class="form-group now">
                    <label for="" class="col-sm-3 col-form-label">Product name</label>
                    <div class="col-sm-9">
                        <input type="text" class="form-control">
                    </div>
                </div>
                
                <div class="form-group now">
                    <label for="" class="col-sm-3 col-form-label">Product name</label>
                    <div class="col-sm-9">
                        <input type="text" class="form-control">
                    </div>
                </div>

                <div class="form-group now">
                    <label for="" class="col-sm-3 col-form-label">Product name</label>
                    <div class="col-sm-9">
                        <textarea name="" id="" cols="30" rows="10"></textarea>
                    </div>
                </div>

                <div class="form-group now">
                   <button type="submit" class="btn btn-success">Save</button>
                   <button type="reset" class="btn btn-danger">Cancel</button>
                </div>                
            </form>
        </div>
    </div>
</template>