<template>
    <div>
        <CRow>
            <CCol sm="6" lg="3" @click="changeCard('sales')">
                <!--  -->
                <CWidgetProgress :class="cardSelected === 'sales' ? 'card-selected' : 'card-unselected'" style="cursor: pointer">
                    <div class="h4 m-0 font-weight-bold">Sales</div>
                    <div class="py-3">
                        <CRow>
                            <CCol col="6" class="py-4">
                                <CButton block color="info p-0" shape="pill" style="width: 60px">
                                    20%
                                </CButton>
                            </CCol>
                            <CCol col="6">
                                <span class="float-right" style="font-size: 10px; color: #cccccc">Lifetime Sales</span>
                                <span class="float-right font-weight-bold">
                                    <span class="text-warning">P</span>
                                    175,000
                                </span>
                                <span class="float-right" style="font-size: 10px; color: #cccccc">Revenue Sales</span>
                                <span class="float-right font-weight-bold">
                                    <span class="text-warning">P</span>
                                    170,000
                                </span>
                            </CCol>
                        </CRow>
                    </div>
                    <hr class="m-0 mb-1">
                    <span style="color: #cccccc; font-size: 10px;">Average Order Value</span>
                    <span style="color: #cccccc; font-size: 10px;" class="float-right pt-1">
                        <span class="text-warning font-weight-bold">P</span>
                        1,000.00
                    </span>
                </CWidgetProgress>
            </CCol>
            <CCol sm="6" lg="3" @click="changeCard('engagement')">
                <CWidgetProgress :class="cardSelected === 'engagement' ? 'card-selected' : 'card-unselected'" style="cursor: pointer">
                    <div class="h4 m-0 font-weight-bold">Engagement</div>
                    <div class="py-3">
                        <CRow>
                            <CCol col="6" class="py-4">
                                <CButton block color="success p-0" shape="pill" style="width: 60px">
                                    20%
                                </CButton>
                            </CCol>
                            <CCol col="6">
                                <CRow>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Lifetime SMS</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            285
                                        </span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Daily Average</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            57
                                        </span>
                                    </CCol>
                                </CRow>
                            </CCol>
                        </CRow>
                    </div>
                    <hr class="m-0 mb-1">
                    <span style="color: #cccccc; font-size: 10px;">20% decrease in 30 days</span>
                </CWidgetProgress>
            </CCol>
            <CCol sm="6" lg="3" @click="changeCard('acquisition')">
                <CWidgetProgress :class="cardSelected === 'acquisition' ? 'card-selected' : 'card-unselected'" style="cursor: pointer">
                    <div class="h4 m-0 font-weight-bold">Acquisition</div>
                    <div class="py-3">
                        <CRow>
                            <CCol col="6" class="py-4">
                                <CButton block color="warning text-white p-0" shape="pill" style="width: 60px">
                                    20%
                                </CButton>
                            </CCol>
                            <CCol col="6">
                                <CRow>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Registered Users</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            285
                                        </span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Daily Average</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            57
                                        </span>
                                    </CCol>
                                </CRow>
                            </CCol>
                        </CRow>
                    </div>
                    <hr class="m-0 mb-1">
                    <span style="color: #cccccc; font-size: 10px;">20% increase in 30 days</span>
                </CWidgetProgress>
            </CCol>
            <CCol sm="6" lg="3" @click="changeCard('rewards')">
                <CWidgetProgress :class="cardSelected === 'rewards' ? 'card-selected' : 'card-unselected'" style="cursor: pointer">
                    <div class="h4 m-0 font-weight-bold">Rewards Program</div>
                    <div class="py-3">
                        <CRow>
                            <CCol col="6" class="py-4">
                                <CButton block color="primary text-white p-0" shape="pill" style="width: 60px">
                                    20%
                                </CButton>
                            </CCol>
                            <CCol col="6">
                                <CRow>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Rewards Redeemed</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            175,000
                                        </span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right" style="font-size: 10px; color: #cccccc">Issued Rewards</span>
                                    </CCol>
                                    <CCol col="12">
                                        <span class="float-right font-weight-bold">
                                            175,000
                                        </span>
                                    </CCol>
                                </CRow>
                            </CCol>
                        </CRow>
                    </div>
                    <hr class="m-0 mb-1">
                    <span style="color: #cccccc; font-size: 10px;">20% increase in 30 days</span>
                </CWidgetProgress>
            </CCol>
        </CRow>
        <CRow>
            <CCol sm="6" lg="3">
                <CSelect
                    :options="['Last 7 days','Last 6 days','Last 5 days']"
                />
            </CCol>
            <CCol sm="6" lg="3">
                <CInput
                    type="date"
                    horizontal
                />
            </CCol>
        </CRow>
        <CCard v-show="cardSelected==='sales'">
            <CCardHeader class="d-flex"><b>Sales Overview</b>
            </CCardHeader>
            <CCardBody><CChartBarExample/></CCardBody>
        </CCard>
        <CCard v-show="cardSelected==='engagement'">
            <CCardHeader class="d-flex"><b>Engagement Overview</b>
            </CCardHeader>
            <CCardBody>
                <MainChartExample style="height:300px;margin-top:40px;"/>
            </CCardBody>
        </CCard>
        <CCard v-show="cardSelected==='acquisition'">
            <CCardHeader class="d-flex"><b>Acquisition Overview</b>
            </CCardHeader>
            <CCardBody>
                <CChartLineExample/>
            </CCardBody>
        </CCard>
        <CCard v-show="cardSelected==='rewards'">
            <CCardHeader class="d-flex"><b>Rewards Overview</b>
            </CCardHeader>
            <CCardBody><CChartPieExample/></CCardBody>
        </CCard>
    </div>
</template>
<script>
import * as Charts from './charts/index.js'
import MainChartExample from './charts/MainChartExample'
import axios from 'axios'
export default {
    name: 'Home',
    components: {
        ...Charts,
        MainChartExample
    },
    created () {
        // READY FOR API REQUEST
        // const res = axios.get('https://6076b1961ed0ae0017d69919.mockapi.io/api/v1/asticom')
        // console.log('created', res);
    },
    data: () => ({
        cardSelected: 'sales'
    }),
    methods: {
        changeCard (selected) {
            this.cardSelected = selected;
        }
    }
}
</script>
<style scoped>
    .card-selected {
        border-style: solid;
        border-color: #90a6f1;
        border-width: 3px;
    }
    .card-unselected {
        background-color: #d9d9d9
    }
</style>