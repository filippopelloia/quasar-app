<template>
    <q-page class="flex flex-center" padding>
        <div class="full-width" style="max-width: 350px;">
            <h5 class="q-my-md text-center">Login</h5>
            <q-card>
                <q-card-section>
                    <q-form>
                        <q-input filled label="email" placeholder="email@example.com" class="q-mb-md" />
                        <q-input filled label="password" type="password" class="q-mb-sm" />
                        <q-checkbox :model-value="true" label="remember me" />
                    </q-form>
                </q-card-section>
                <q-btn label="login" class="full-width" color="primary" />
            </q-card>
        </div>
    </q-page>
</template>
