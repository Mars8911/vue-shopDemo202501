<template>
    <!-- Modal -->
    <div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel"
        ref="model">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    ...
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                    <button type="button" class="btn btn-primary">Save changes</button>
                </div>
            </div>
        </div>
    </div>
</template>



<script>
import Model from 'bootstrap/js/dist/modal'
export default {
    data() {
        return {
            model: {}
        }
    },
    methods: {
        showModel() {
            this.modal.show();
        },

        hideModel() {
            this.modal.hide();
        }

    },
    mounted() {
        this.modal = new Model(this.$refs.model)
        this.hideModel()
    }
}
</script>