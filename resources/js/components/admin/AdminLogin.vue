<template>
    <Form @submit="onSubmit" :validation-schema="schema" v-slot="{ errors }">
        <div class="form-row">
            <div class="form-group col-5">
                <label>Username</label>
                    <Field name="username" type="text" class="form-control" :class="{ 'is-invalid': errors.username }" />
                <div class="invalid-feedback">{{errors.username}}</div>
            </div>
            <div class="form-group col-5">
                <label>Password</label>
                    <Field name="password" type="text" class="form-control" :class="{ 'is-invalid': errors.password }" />
                <div class="invalid-feedback">{{errors.password }}</div>
            </div>
        </div>      
        <div class="form-group">
            <button type="submit" class="mr-1 btn btn-primary">Login</button>
            <button type="reset" class="btn btn-secondary">Reset</button>
        </div>
    </Form>
</template>
<script>
import { Form, Field } from 'vee-validate';

export default {
    components: {
        Form,
        Field,
    },
}
</script>

