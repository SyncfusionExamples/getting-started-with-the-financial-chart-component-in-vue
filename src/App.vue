<template>
  <div id="app">
    <ejs-chart :primaryXAxis="chartPrimaryXAxis" :title="chartTitle"
    :primaryYAxis="chartPrimaryYAxis" :tooltip="chartTooltip"
    :crosshair="chartCrosshairSettings">
      <e-series-collection>
        <e-series type="Candle" :dataSource="stockData" xName="date" high="highValue"
        low="lowValue" open="openValue" close="closeValue" volume="volumeValue">
        </e-series>
      </e-series-collection>
    </ejs-chart>
  </div>
</template>

<script>
import Vue from "vue";
import { ChartPlugin, HiloSeries, DateTime, Tooltip, Crosshair, HiloOpenCloseSeries,
CandleSeries } from '@syncfusion/ej2-vue-charts';
Vue.use(ChartPlugin);

export default {
  provide : {
    chart : [HiloSeries, DateTime, Tooltip, Crosshair, HiloOpenCloseSeries, CandleSeries]
  },
  data() {
    return {
      chartCrosshairSettings : {
        enable : true,
        lineType : 'Vertical'
      },
      chartTooltip : {
        enable : true
      },
      chartPrimaryYAxis: {
        title : 'Price in Dollars'
      },
      chartTitle: 'Financial Analysis',
      chartPrimaryXAxis : {
        title: 'DateTime',
        valueType : 'DateTime',
        minimum: new Date('2019-12-31'),
        maximum: new Date('2021-09-30')
      },
      stockData : [
      {
        date: new Date( '2020-01-04' ),
        openValue : 102.61,
        highValue : 105.85,
        lowValue : 96.43,
        closeValue : 96.96,
        volumeValue : 343000960
      },
      {
        date: new Date( '2020-01-11' ),
        openValue : 98.97,
        highValue : 101.19,
        lowValue : 95.36,
        closeValue : 97.13,
        volumeValue : 303375940
      },
      {
        date: new Date( '2020-01-18' ),
        openValue : 98.41,
        highValue : 101.46,
        lowValue : 93.42,
        closeValue : 101.42,
        volumeValue : 242982970
      },
      {
        date: new Date( '2020-01-25' ),
        openValue : 101.52,
        highValue : 101.53,
        lowValue : 92.39,
        closeValue : 97.34,
        volumeValue : 376481100
      },
      {
        date: new Date( '2020-02-01' ),
        openValue : 96.47,
        highValue : 97.33,
        lowValue : 93.69,
        closeValue : 94.02,
        volumeValue : 216608840
      },
      {
        date: new Date( '2020-02-08' ),
        openValue : 93.13,
        highValue : 96.35,
        lowValue : 92.59,
        closeValue : 93.99,
        volumeValue : 230794620
      },
      {
        date: new Date( '2020-02-15' ),
        openValue : 95.02,
        highValue : 98.89,
        lowValue : 94.61,
        closeValue : 96.04,
        volumeValue : 167001070
      },
      {
        date: new Date( '2020-02-22' ),
        openValue : 96.31,
        highValue : 98.0237,
        lowValue : 93.32,
        closeValue : 96.91,
        volumeValue : 158759600
      },
      {
        date: new Date( '2020-02-29' ),
        openValue : 96.86,
        highValue : 103.75,
        lowValue : 96.65,
        closeValue : 103.01,
        volumeValue : 201482180
      },
      {
        date: new Date( '2020-03-07' ),
        openValue : 102.39,
        highValue : 102.83,
        lowValue : 100.15,
        closeValue : 102.26,
        volumeValue : 155437450
      },
      {
        date: new Date( '2020-03-14' ),
        openValue : 101.91,
        highValue : 106.5,
        lowValue : 101.78,
        closeValue : 105.92,
        volumeValue : 181323210
      },
      {
        date: new Date( '2020-03-21' ),
        openValue : 105.93,
        highValue : 107.65,
        lowValue : 104.89,
        closeValue : 105.67,
        volumeValue : 119054360
      },
      {
        date: new Date( '2020-03-28' ),
        openValue : 106,
        highValue : 110.42,
        lowValue : 104.88,
        closeValue : 109.99,
        volumeValue : 147641240
      },
      {
        date: new Date( '2020-04-04' ),
        openValue : 110.42,
        highValue : 112.19,
        lowValue : 108.121,
        closeValue : 108.66,
        volumeValue : 145351790
      },
      {
        date: new Date( '2020-04-11' ),
        openValue : 108.97,
        highValue : 112.39,
        lowValue : 108.66,
        closeValue : 109.85,
        volumeValue : 161518860
      },
      {
        date: new Date( '2020-04-18' ),
        openValue : 108.89,
        highValue : 108.95,
        lowValue : 104.62,
        closeValue : 105.68,
        volumeValue : 188775240
      },
      {
        date: new Date( '2020-04-25' ),
        openValue : 105,
        highValue : 105.65,
        lowValue : 92.51,
        closeValue : 93.74,
        volumeValue : 345910030
      },
      {
        date: new Date( '2020-05-02' ),
        openValue : 93.965,
        highValue : 95.9,
        lowValue : 91.85,
        closeValue : 92.72,
        volumeValue : 225114110
      },
      {
        date: new Date( '2020-05-09' ),
        openValue : 93,
        highValue : 93.77,
        lowValue : 89.47,
        closeValue : 90.52,
        volumeValue : 215596350
      },
      {
        date: new Date( '2020-05-16' ),
        openValue : 92.39,
        highValue : 95.43,
        lowValue : 91.65,
        closeValue : 95.22,
        volumeValue : 212312980
      },
      {
        date: new Date( '2020-05-23' ),
        openValue : 95.87,
        highValue : 100.73,
        lowValue : 95.67,
        closeValue : 100.35,
        volumeValue : 203902650
      },
      {
        date: new Date( '2020-05-30' ),
        openValue : 99.6,
        highValue : 100.4,
        lowValue : 96.63,
        closeValue : 97.92,
        volumeValue : 140064910
      },
      {
        date: new Date( '2020-06-06' ),
        openValue : 97.99,
        highValue : 101.89,
        lowValue : 97.55,
        closeValue : 98.83,
        volumeValue : 124731320
      },
      {
        date: new Date( '2020-06-13' ),
        openValue : 98.69,
        highValue : 99.12,
        lowValue : 95.3,
        closeValue : 95.33,
        volumeValue : 191017280
      },
      {
        date: new Date( '2020-06-20' ),
        openValue : 96,
        highValue : 96.89,
        lowValue : 92.65,
        closeValue : 93.4,
        volumeValue : 206149160
      },
      {
        date: new Date( '2020-06-27' ),
        openValue : 93,
        highValue : 96.465,
        lowValue : 91.5,
        closeValue : 95.89,
        volumeValue : 184254460
      },
      {
        date: new Date( '2020-07-04' ),
        openValue : 95.39,
        highValue : 96.89,
        lowValue : 94.37,
        closeValue : 96.68,
        volumeValue : 111769640
      },
      {
        date: new Date( '2020-07-11' ),
        openValue : 96.75,
        highValue : 99.3,
        lowValue : 96.73,
        closeValue : 98.78,
        volumeValue : 142244590
      },
      {
        date: new Date( '2020-07-18' ),
        openValue : 98.7,
        highValue : 101,
        lowValue : 98.31,
        closeValue : 98.66,
        volumeValue : 147358320
      },
      {
        date: new Date( '2020-07-25' ),
        openValue : 98.25,
        highValue : 104.55,
        lowValue : 96.42,
        closeValue : 104.21,
        volumeValue : 252358930
      },
      {
        date: new Date( '2020-08-01' ),
        openValue : 104.41,
        highValue : 107.65,
        lowValue : 104,
        closeValue : 107.48,
        volumeValue : 168265830
      },
      {
        date: new Date( '2020-08-08' ),
        openValue : 107.52,
        highValue : 108.94,
        lowValue : 107.16,
        closeValue : 108.18,
        volumeValue : 124255340
      },
      {
        date: new Date( '2020-08-15' ),
        openValue : 108.14,
        highValue : 110.23,
        lowValue : 108.08,
        closeValue : 109.36,
        volumeValue : 131814920
      },
      {
        date: new Date( '2020-08-22' ),
        openValue : 108.86,
        highValue : 109.32,
        lowValue : 106.31,
        closeValue : 106.94,
        volumeValue : 123373540
      },
      {
        date: new Date( '2020-08-29' ),
        openValue : 106.62,
        highValue : 108,
        lowValue : 105.5,
        closeValue : 107.73,
        volumeValue : 134426100
      },
      {
        date: new Date( '2020-09-05' ),
        openValue : 107.9,
        highValue : 108.76,
        lowValue : 103.13,
        closeValue : 103.13,
        volumeValue : 168312530
      },
      {
        date: new Date( '2020-09-12' ),
        openValue : 102.65,
        highValue : 116.13,
        lowValue : 102.53,
        closeValue : 114.92,
        volumeValue : 388543710
      },
      {
        date: new Date( '2020-09-19' ),
        openValue : 115.19,
        highValue : 116.18,
        lowValue : 111.55,
        closeValue : 112.71,
        volumeValue : 200842480
      },
      {
        date: new Date( '2020-09-26' ),
        openValue : 111.64,
        highValue : 114.64,
        lowValue : 111.55,
        closeValue : 113.05,
        volumeValue : 156186800
      },
      {
        date: new Date( '2020-10-03' ),
        openValue : 112.71,
        highValue : 114.56,
        lowValue : 112.28,
        closeValue : 114.06,
        volumeValue : 125587350
      },
      {
        date: new Date( '2020-10-10' ),
        openValue : 115.02,
        highValue : 118.69,
        lowValue : 114.72,
        closeValue : 117.63,
        volumeValue : 208231690
      },
      {
        date: new Date( '2020-10-17' ),
        openValue : 117.33,
        highValue : 118.21,
        lowValue : 113.8,
        closeValue : 116.6,
        volumeValue : 114497020
      },
      {
        date: new Date( '2020-10-24' ),
        openValue : 117.1,
        highValue : 118.36,
        lowValue : 113.31,
        closeValue : 113.72,
        volumeValue : 204530120
      },
      {
        date: new Date( '2020-10-31' ),
        openValue : 113.65,
        highValue : 114.23,
        lowValue : 108.11,
        closeValue : 108.84,
        volumeValue : 155287280
      },
      {
        date: new Date( '2020-11-07' ),
        openValue : 110.08,
        highValue : 111.72,
        lowValue : 105.83,
        closeValue : 108.43,
        volumeValue : 206825070
      },
      {
        date: new Date( '2020-11-14' ),
        openValue : 107.71,
        highValue : 110.54,
        lowValue : 104.08,
        closeValue : 110.06,
        volumeValue : 197790040
      },
      {
        date: new Date( '2020-11-21' ),
        openValue : 110.12,
        highValue : 112.42,
        lowValue : 110.01,
        closeValue : 111.79,
        volumeValue : 93992370
      },
      {
        date: new Date( '2020-11-28' ),
        openValue : 111.43,
        highValue : 112.465,
        lowValue : 108.85,
        closeValue : 109.9,
        volumeValue : 155229390
      },
      {
        date: new Date( '2020-12-05' ),
        openValue : 110,
        highValue : 114.7,
        lowValue : 108.25,
        closeValue : 113.95,
        volumeValue : 151624650
      },
      {
        date: new Date( '2020-12-12' ),
        openValue : 113.29,
        highValue : 116.73,
        lowValue : 112.49,
        closeValue : 115.97,
        volumeValue : 194003220
      },
      {
        date: new Date( '2020-12-19' ),
        openValue : 115.8,
        highValue : 117.5,
        lowValue : 115.59,
        closeValue : 116.52,
        volumeValue : 113106370
      },
      {
        date: new Date( '2020-12-26' ),
        openValue : 116.52,
        highValue : 118.0166,
        lowValue : 115.43,
        closeValue : 115.82,
        volumeValue : 84354060
      },
      {
        date: new Date( '2021-01-02' ),
        openValue : 115.8,
        highValue : 118.16,
        lowValue : 114.76,
        closeValue : 117.91,
        volumeValue : 103680760
      },
      {
        date: new Date( '2021-01-09' ),
        openValue : 117.95,
        highValue : 119.93,
        lowValue : 117.94,
        closeValue : 119.04,
        volumeValue : 138446660
      },
      {
        date: new Date( '2021-01-16' ),
        openValue : 118.34,
        highValue : 120.5,
        lowValue : 118.22,
        closeValue : 120,
        volumeValue : 113576380
      },
      {
        date: new Date( '2021-01-23' ),
        openValue : 120,
        highValue : 122.44,
        lowValue : 119.5,
        closeValue : 121.95,
        volumeValue : 124406640
      },
      {
        date: new Date( '2021-01-30' ),
        openValue : 120.93,
        highValue : 130.49,
        lowValue : 120.62,
        closeValue : 129.08,
        volumeValue : 248063580
      },
      {
        date: new Date( '2021-02-06' ),
        openValue : 129.13,
        highValue : 132.94,
        lowValue : 128.9,
        closeValue : 132.12,
        volumeValue : 136252280
      },
      {
        date: new Date( '2021-02-13' ),
        openValue : 133.08,
        highValue : 136.27,
        lowValue : 132.75,
        closeValue : 135.72,
        volumeValue : 136326260
      },
      {
        date: new Date( '2021-02-20' ),
        openValue : 136.23,
        highValue : 137.48,
        lowValue : 135.28,
        closeValue : 136.66,
        volumeValue : 87773190
      },
      {
        date: new Date( '2021-02-27' ),
        openValue : 137.14,
        highValue : 140.2786,
        lowValue : 136.28,
        closeValue : 139.78,
        volumeValue : 127757050
      },
      {
        date: new Date( '2021-03-06' ),
        openValue : 139.365,
        highValue : 139.98,
        lowValue : 137.05,
        closeValue : 139.14,
        volumeValue : 99061270
      },
      {
        date: new Date( '2021-03-13' ),
        openValue : 138.85,
        highValue : 141.02,
        lowValue : 138.82,
        closeValue : 139.99,
        volumeValue : 120881720
      },
      {
        date: new Date( '2021-03-20' ),
        openValue : 140.4,
        highValue : 142.8,
        lowValue : 139.73,
        closeValue : 140.64,
        volumeValue : 129178500
      },
      {
        date: new Date( '2021-03-27' ),
        openValue : 139.39,
        highValue : 144.5,
        lowValue : 138.62,
        closeValue : 143.66,
        volumeValue : 126819590
      },
      {
        date: new Date( '2021-04-03' ),
        openValue : 143.71,
        highValue : 145.46,
        lowValue : 143.05,
        closeValue : 143.34,
        volumeValue : 105274540
      },
      {
        date: new Date( '2021-04-10' ),
        openValue : 143.6,
        highValue : 143.8792,
        lowValue : 140.06,
        closeValue : 141.05,
        volumeValue : 87342130
      },
      {
        date: new Date( '2021-04-17' ),
        openValue : 141.48,
        highValue : 142.92,
        lowValue : 140.45,
        closeValue : 142.27,
        volumeValue : 89092650
      },
      {
        date: new Date( '2021-04-24' ),
        openValue : 143.5,
        highValue : 144.9,
        lowValue : 143.18,
        closeValue : 143.65,
        volumeValue : 90423600
      },
      {
        date: new Date( '2021-05-01' ),
        openValue : 145.1,
        highValue : 148.98,
        lowValue : 144.27,
        closeValue : 148.96,
        volumeValue : 173861760
      },
      {
        date: new Date( '2021-05-08' ),
        openValue : 149.03,
        highValue : 156.42,
        lowValue : 149.03,
        closeValue : 156.1,
        volumeValue : 173087500
      },
      {
        date: new Date( '2021-05-15' ),
        openValue : 156.01,
        highValue : 156.65,
        lowValue : 149.71,
        closeValue : 153.06,
        volumeValue : 156993820
      },
      {
        date: new Date( '2021-05-22' ),
        openValue : 154,
        highValue : 154.9,
        lowValue : 152.67,
        closeValue : 153.61,
        volumeValue : 103151450
      },
      {
        date: new Date( '2021-05-29' ),
        openValue : 153.42,
        highValue : 155.45,
        lowValue : 152.22,
        closeValue : 155.45,
        volumeValue : 88670120
      },
      {
        date: new Date( '2021-06-05' ),
        openValue : 154.34,
        highValue : 155.98,
        lowValue : 146.02,
        closeValue : 148.98,
        volumeValue : 158814040
      },
      {
        date: new Date( '2021-06-12' ),
        openValue : 145.74,
        highValue : 147.5,
        lowValue : 142.2,
        closeValue : 142.27,
        volumeValue : 219638930
      },
      {
        date: new Date( '2021-06-19' ),
        openValue : 143.66,
        highValue : 147.16,
        lowValue : 143.66,
        closeValue : 146.28,
        volumeValue : 132832660
      },
      {
        date: new Date( '2021-06-26' ),
        openValue : 147.17,
        highValue : 148.28,
        lowValue : 142.28,
        closeValue : 144.02,
        volumeValue : 126890110
      },
      {
        date: new Date( '2021-07-03' ),
        openValue : 144.88,
        highValue : 145.3001,
        lowValue : 142.41,
        closeValue : 144.18,
        volumeValue : 78465450
      },
      {
        date: new Date( '2021-07-10' ),
        openValue : 144.11,
        highValue : 149.33,
        lowValue : 143.37,
        closeValue : 149.04,
        volumeValue : 109759170
      },
      {
        date: new Date( '2021-07-17' ),
        openValue : 148.82,
        highValue : 151.74,
        lowValue : 148.57,
        closeValue : 150.27,
        volumeValue : 104744470
      },
      {
        date: new Date( '2021-07-24' ),
        openValue : 150.58,
        highValue : 153.99,
        lowValue : 147.3,
        closeValue : 149.5,
        volumeValue : 105536280
      },
      {
        date: new Date( '2021-07-31' ),
        openValue : 149.9,
        highValue : 159.75,
        lowValue : 148.13,
        closeValue : 156.39,
        volumeValue : 170204830
      },
      {
        date: new Date( '2021-08-07' ),
        openValue : 157.06,
        highValue : 161.83,
        lowValue : 154.63,
        closeValue : 157.48,
        volumeValue : 149860480
      },
      {
        date: new Date( '2021-08-14' ),
        openValue : 159.32,
        highValue : 162.51,
        lowValue : 156.72,
        closeValue : 157.5,
        volumeValue : 133829670
      },
      {
        date: new Date( '2021-08-21' ),
        openValue : 157.5,
        highValue : 160.74,
        lowValue : 155.1101,
        closeValue : 159.86,
        volumeValue : 112238670
      },
      {
        date: new Date( '2021-08-28' ),
        openValue : 160.14,
        highValue : 164.94,
        lowValue : 159.93,
        closeValue : 164.05,
        volumeValue : 125610990
      },
      {
        date: new Date( '2021-09-04' ),
        openValue : 163.75,
        highValue : 164.25,
        lowValue : 158.53,
        closeValue : 158.63,
        volumeValue : 101419110
      },
      {
        date: new Date( '2021-09-11' ),
        openValue : 160.5,
        highValue : 163.96,
        lowValue : 157.91,
        closeValue : 159.88,
        volumeValue : 220431100
      },
      {
        date: new Date( '2021-09-18' ),
        openValue : 160.11,
        highValue : 160.5,
        lowValue : 157.995,
        closeValue : 158.67,
        volumeValue : 27939544
      }
      ]
    };
  }
 
}
</script>

<style>

</style>
