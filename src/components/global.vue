<template>
<div>
    <b-card bg-variant="light" class="card_margin">
        <b-form-group label-cols-lg="3" label="Global Parameter" label-size="lg" label-class="font-weight-bold pt-0" class="mb-0">
            <b-form-group label-cols-sm="3" label="Days of LB:" label-align-sm="right" label-for="days_of_lb">
                <b-form-select id="days_of_lb" v-model="selected" :options="lb_options"></b-form-select>
            </b-form-group>
            <div class="action_div">
                <b-button class="clear_cachec-_btn" variant="light">Clear Cache</b-button>
                <b-button variant="primary">Submit</b-button>
            </div>
        </b-form-group>

    </b-card>
    <div class="table_div">
        <b-table striped bordered sticky-header hover :items="items">
            <template v-slot:cell(strore)="row">
                <!--<b-nav-item href="javascript:void(0)" v-model="row.detailsShowing" @click="scrollIntoView">{{row.value}}</b-nav-item> -->
                <b-nav-item to="#id-of-element" v-model="row.detailsShowing">{{row.value}}</b-nav-item>
            </template>
            <template v-slot:cell(LB)="row">
                <b-form-checkbox v-model="row.detailsShowing" name="check-button" switch><b>YES</b>
                </b-form-checkbox>
            </template>
        </b-table>
    </div>
    <!-- <b-card bg-variant="light" class="card_margin">

    </b-card> -->
</div>
</template>

<script>
export default {
    name: 'globalScreen',
    data() {
        return {
            selected: null,
            lb_options: [{
                    value: null,
                    text: 'Please select an option'
                },
                {
                    value: '1',
                    text: '1'
                },
                {
                    value: '2',
                    text: '2'
                },
                {
                    value: "3",
                    text: '3'
                },
                {
                    value: '4',
                    text: '4'
                },
                {
                    value: '5',
                    text: '5'
                }
            ],
            items: [{
                    strore: "GKB",
                    LB: '',
                },
                {
                    strore: "GiJ",
                    LB: '',
                },
                {
                    strore: "GiJ",
                    LB: '',
                },
                {
                    strore: "GiJ",
                    LB: '',
                }
            ]
        }
    }
}
</script>

<style scoped>
.action_div {
    text-align: end;
}

.clear_cachec-_btn {
    margin-right: 10px;
}

.card_margin {
    margin: 15px;
}

.table_div {
    margin: 15px;
}

li {
    list-style-type: none;
}
</style>
