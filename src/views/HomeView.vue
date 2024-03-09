<template>
  <div class="container">
    <div class="grid_line1">
      <div class="card">
        <img src="../assets/icons/eject.svg" alt="" />
        <div>
          <h1>Uptime</h1>
          <p>Uptime over the past 24 hours</p>
          <div>
            <span>97.83%</span>
            <CanvasJSChart :options="options" :styles="styleOptions" />
          </div>
        </div>
      </div>
      <div class="globus_card">
        <h1>Waxpeer online & status</h1>
        <div class="card2">
          <div>
            <div class="grid_line3">
              <div>
                <span>12698</span>
                <p>extension</p>
              </div>
              <div class="left_border">
                <span>5898</span>
                <p>desktop</p>
              </div>
              <div class="left_border">
                <span>25697</span>
                <p>mobile</p>
              </div>
            </div>
          </div>
          <div class="globus">
            <img class="g_item" src="../assets/img/Ellipse 142.svg" alt="" />
            <span class="g_item axis axis1"></span>
            <span class="g_item axis axis2"></span>
            <span class="g_item axis axis3"></span>
            <h3 class="g_item">Styable</h3>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/eject.svg" alt="" />
        <div>
          <h1>Current date</h1>
          <p>Current date and time</p>
          <div>
            <span>08.06.2022</span>
            <p>19:55:20</p>
          </div>
        </div>
      </div>
    </div>
    <div class="grid_line2">
      <div class="card">
        <img src="../assets/icons/bitcoin.svg" alt="" />
        <div>
          <h1>Withdrawal status</h1>
          <p>Connected cryptocurrencies</p>
          <div>
            <img src="../assets/icons/Subtract.svg" alt="" />
            <img src="../assets/icons/Subtract2.svg" alt="" />
            <img src="../assets/icons/Subtract3.svg" alt="" />
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/dollar.svg" alt="" />
        <div>
          <h1>Buy items</h1>
          <p>Time from the last purchase</p>
          <div>
            <span>25 sec</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/bot.svg" alt="" />
        <div>
          <h1>Waxpeer pay bots</h1>
          <p>The number of avaliable bots on Waxpeer pay</p>
          <div>
            <span>259 bots</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/pay.svg" alt="" />
        <div>
          <h1>Waxpeer pay</h1>
          <p>The last successful trade</p>
          <div>
            <span>10 sec</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/site.svg" alt="" />
        <div>
          <h1>Availability of a site</h1>
          <p>The availability of the home page of the site</p>
          <div>
            <span class="green">available</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/cloud.svg" alt="" />
        <div>
          <h1>Server status</h1>
          <p>The status of the website servers</p>
          <div>
            <span class="warning">unstable</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/steam.svg" alt="" />
        <div>
          <h1>Steam Web API</h1>
          <p>Last check June 3, 2022 02:50:16</p>
          <div>
            <span class="green">stable</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/setting.svg" alt="" />
        <div>
          <h1>API response</h1>
          <p>Last request 10 seconds ago</p>
          <div>
            <span class="green">2.856 ms</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/cart.svg" alt="" />
        <div>
          <h1>Last trade</h1>
          <p>The last trade was created 5s ago</p>
          <div>
            <span class="cancel">canceled</span>
          </div>
        </div>
      </div>
      <div class="card">
        <img src="../assets/icons/user.svg" alt="" />
        <div>
          <h1>Login</h1>
          <p>Shows either your login is working or not</p>
          <div>
            <span class="green">active</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
import * as CanvasJS from '@canvasjs/charts'
import { ref } from 'vue'
const options = ref({
  theme: 'dark1',
  animationEnabled: true,
  backgroundColor: false,
  title: {},
  axisY: {
    tickLength: 0,
    gridThickness: 0,
    labelFormatter: function () {
      return ''
    }
  },
  axisX: {
    tickLength: 0,
    labelFormatter: function () {
      return ''
    }
  },
  toolTip: {
    shared: true,
    contentFormatter: function (e) {
      return CanvasJS.formatNumber(e.entries[0].dataPoint.y / 1000000000000, '#.#0')
    }
  },
  data: [
    {
      color: '#eeeeee10',
      type: 'splineArea',
      lineColor: '#ffffff',
      dataPoints: [
        { label: '2009', y: 3644702000000, markerType: 'null' },
        { label: '2010', y: 3788321000000, markerType: 'null' },
        { label: '2011', y: 3779423000000, markerType: 'null' },
        { label: '2012', y: 3726774000000, markerType: 'null' },
        { label: '2013', y: 3767564000000, markerType: 'null' },
        { label: '2014', y: 3788954000000, markerType: 'null' },
        { label: '2015', y: 3780836000000, markerType: 'null' },
        { label: '2016', y: 3807711000000, markerType: 'null' }
      ]
    }
  ]
})
const styleOptions = ref({
  width: '150px',
  height: '60px'
})
</script>
<style scoped></style>
