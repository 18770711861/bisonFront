<template>
  <div class="animated fadeIn">
    <div class="row">
      <div class="col-sm-6 col-lg-3">
        <div class="card card-inverse card-primary">
          <div class="card-block pb-0">
            <dropdown class="float-right" type="transparent p-0">
              <i slot="button" class="icon-settings"></i>
              <div slot="dropdown-menu" class="dropdown-menu dropdown-menu-right">
                <a class="dropdown-item" href="#">Action</a>
                <a class="dropdown-item" href="#">Another action</a>
                <a class="dropdown-item" href="#">Something else here</a>
              </div>
            </dropdown>
            <h4 class="mb-0">9.823</h4>
            <p>Members online</p>
          </div>
          <card-line1-chart-example class="chart-wrapper px-3" style="height:70px;" height="70"/>
        </div>
      </div><!--/.col-->

      <div class="col-sm-6 col-lg-3">
        <div class="card card-inverse card-info">
          <div class="card-block pb-0">
            <dropdown class="float-right" type="transparent p-0">
              <i slot="button" class="icon-settings"></i>
              <div slot="dropdown-menu" class="dropdown-menu dropdown-menu-right">
                <a class="dropdown-item" href="#">Action</a>
                <a class="dropdown-item" href="#">Another action</a>
                <a class="dropdown-item" href="#">Something else here</a>
              </div>
            </dropdown>
            <h4 class="mb-0">9.823</h4>
            <p>Members online</p>
          </div>
          <card-line2-chart-example class="chart-wrapper px-3" style="height:70px;" height="70"/>
        </div>
      </div><!--/.col-->

      <div class="col-sm-6 col-lg-3">
        <div class="card card-inverse card-warning">
          <div class="card-block pb-0">
            <div class="btn-group float-right">
              <dropdown class="float-right" type="transparent p-0">
                <i slot="button" class="icon-settings"></i>
                <div slot="dropdown-menu" class="dropdown-menu dropdown-menu-right">
                  <a class="dropdown-item" href="#">Action</a>
                  <a class="dropdown-item" href="#">Another action</a>
                  <a class="dropdown-item" href="#">Something else here</a>
                </div>
              </dropdown>
            </div>
            <h4 class="mb-0">9.823</h4>
            <p>Members online</p>
          </div>
          <card-line3-chart-example class="chart-wrapper" style="height:70px;" height="70"/>
        </div>
      </div><!--/.col-->

      <div class="col-sm-6 col-lg-3">
        <div class="card card-inverse card-danger">
          <div class="card-block pb-0">
            <div class="btn-group float-right">
              <dropdown class="float-right" type="transparent p-0">
                <i slot="button" class="icon-settings"></i>
                <div slot="dropdown-menu" class="dropdown-menu dropdown-menu-right">
                  <a class="dropdown-item" href="#">Action</a>
                  <a class="dropdown-item" href="#">Another action</a>
                  <a class="dropdown-item" href="#">Something else here</a>
                </div>
              </dropdown>
            </div>
            <h4 class="mb-0">9.823</h4>
            <p>Members online</p>
          </div>
          <card-bar-chart-example class="chart-wrapper px-3" style="height:70px;" height="70"/>
        </div>
      </div><!--/.col-->
    </div><!--/.row-->   
  </div>
</template>

<script>
import CardLine1ChartExample from './dashboard/CardLine1ChartExample'
import CardLine2ChartExample from './dashboard/CardLine2ChartExample'
import CardLine3ChartExample from './dashboard/CardLine3ChartExample'
import CardBarChartExample from './dashboard/CardBarChartExample'
import MainChartExample from './dashboard/MainChartExample'
import SocialBoxChartExample from './dashboard/SocialBoxChartExample'

import { dropdown } from 'vue-strap'

export default {
  name: 'dashboard',
  components: {
    CardLine1ChartExample,
    CardLine2ChartExample,
    CardLine3ChartExample,
    CardBarChartExample,
    MainChartExample,
    SocialBoxChartExample,
    dropdown
  }
}
</script>
