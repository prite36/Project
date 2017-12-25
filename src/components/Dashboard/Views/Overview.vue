<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <!-- <div class="col-xl-3 col-md-6">
          <stats-card>
            <div slot="header" class="icon-warning">
              <i class="nc-icon nc-chart text-warning"></i>
            </div>
            <div slot="content">
              <p class="card-category">Capacity</p>
              <h4 class="card-title">105GB</h4>
            </div>
            <div slot="footer">
              <i class="fa fa-refresh"></i>Updated now
            </div>
          </stats-card>
        </div> -->

        <!-- <div class="col-xl-3 col-md-6">
          <stats-card>
            <div slot="header" class="icon-success">
              <i class="nc-icon nc-light-3 text-success"></i>
            </div>
            <div slot="content">
              <p class="card-category">Revenue</p>
              <h4 class="card-title">$1,345</h4>
            </div>
            <div slot="footer">
              <i class="fa fa-calendar-o"></i>Last day
            </div>
          </stats-card>
        </div> -->

        <!-- <div class="col-xl-3 col-md-6">
          <stats-card>
            <div slot="header" class="icon-danger">
              <i class="nc-icon nc-vector text-danger"></i>
            </div>
            <div slot="content">
              <p class="card-category">Errors</p>
              <h4 class="card-title">23</h4>
            </div>
            <div slot="footer">
              <i class="fa fa-clock-o"></i>Last day
            </div>
          </stats-card>
        </div> -->

        <!-- <div class="col-xl-3 col-md-6">
          <stats-card>
            <div slot="header" class="icon-info">
              <i class="nc-icon nc-favourite-28 text-primary"></i>
            </div>
            <div slot="content">
              <p class="card-category">Followers</p>
              <h4 class="card-title">+45</h4>
            </div>
            <div slot="footer">
              <i class="fa fa-refresh"></i>Updated now
            </div>
          </stats-card>
        </div> -->
      </div>

      <div class="row">
        <!-- <div class="col-md-4">
          <chart-card :chart-data="lineChart.data"
                      :chart-options="lineChart.options"
                      :responsive-options="lineChart.responsiveOptions">
            <template slot="header">
              <h4 class="card-title">Users Behavior</h4>
              <p class="card-category">24 Hours performance</p>
            </template>
            <template slot="footer">
              <div class="legend">
                <i class="fa fa-circle text-info"></i> Open
                <i class="fa fa-circle text-danger"></i> Click
                <i class="fa fa-circle text-warning"></i> Click Second Time
              </div>
              <hr>
              <div class="stats">
                <i class="fa fa-history"></i> Updated 3 minutes ago
              </div>
            </template>
          </chart-card>
        </div> -->

        <div class="col-md-6">
          <chart-card :chart-data="pieChart.data" chart-type="Pie">
            <template slot="header">
              <h4 class="card-title">Email Statistics</h4>
              <p class="card-category">Last Campaign Performance</p>
            </template>
            <template slot="footer">
              <div class="legend">
                <i class="fa fa-circle text-info"></i> Open
                <i class="fa fa-circle text-danger"></i> Bounce
                <i class="fa fa-circle text-warning"></i> Unsubscribe
              </div>
              <hr>
              <div class="stats">

                <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModalA">
                  Launch demo modal A
                </button>

              </div>
            </template>
          </chart-card>
        </div>

        <div class="col-md-6">
          <chart-card
            :chart-data="barChart.data"
            :chart-options="barChart.options"
            :chart-responsive-options="barChart.responsiveOptions"
            chart-type="Bar">
            <template slot="header">
              <h4 class="card-title">2014 Sales</h4>
              <p class="card-category">All products including Taxes</p>
            </template>
            <template slot="footer">
              <div class="legend">
                <i class="fa fa-circle text-info"></i> Tesla Model S
                <i class="fa fa-circle text-danger"></i> BMW 5 Series
              </div>
              <hr>
              <div class="stats">

                <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#exampleModalB">
                  Launch demo modal B
                </button>

              </div>
            </template>
          </chart-card>
        </div>

        งานทั้งหมด : {{ count }} <br>
        To Do : {{ sumall - count }}<br>
        In Progress : {{ sumprogress }} <br>
        Done : {{ donecount }}<br><br>

        Apinan Singbut<br>
        งานทั้งหมดที่ Apinan เป็นคนทำ : {{ ApinanA }}<br>
        งานทั้งหมดที่ Apinan กำลังทำอยู่ : {{ ApinanA - ApinanB }}<br>
        งานทั้งหมดที่ Apinan ทำเสร็จแล้ว : {{ ApinanB }}<br>
        งานทั้งหมดที่ Apinan ทำเสร็จตามเวลา : {{ ApinanOnTime }}<br>
        งานทั้งหมดที่ Apinan ทำเสร็จล่าช้า : {{ ApinanDelay }}<br>

        <!-- Modal A -->
        <div class="modal fade" id="exampleModalA" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
                A
              </div>
              <div class="modal-footer">

              </div>
            </div>
          </div>
        </div>
        <!-- End Modal A -->

        <!-- Modal B -->
        <div class="modal fade" id="exampleModalB" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
                B
              </div>
              <div class="modal-footer">

              </div>
            </div>
          </div>
        </div>
        <!-- End Modal B -->

      </div>

      <div class="row">
        <div class="col-md-6" style="background-color: #FFFFFF">
          <div class="progress">
            <div class="progress-bar progress-bar-striped bg-success" role="progressbar" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
          </div>
          <br>
          <div class="progress">
            <div class="progress-bar progress-bar-striped bg-warning" role="progressbar" style="width: 75%" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100"></div>
          </div>
          <br>
          <div class="progress">
            <div class="progress-bar progress-bar-striped bg-danger" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
          </div>
        </div>

        <div class="col-md-6">
          <chart-card
            :chart-data="barChart.data"
            :chart-options="barChart.options"
            :chart-responsive-options="barChart.responsiveOptions"
            chart-type="Bar">
            <template slot="header">
              <h4 class="card-title">2014 Sales</h4>
              <p class="card-category">All products including Taxes</p>
            </template>
            <template slot="footer">
              <div class="legend">
                <i class="fa fa-circle text-info"></i> Tesla Model S
                <i class="fa fa-circle text-danger"></i> BMW 5 Series
              </div>
            </template>
          </chart-card>
        </div>
      </div>

    </div>
  </div>
</template>
<script>
  import ChartCard from 'src/components/UIComponents/Cards/ChartCard.vue'
  import StatsCard from 'src/components/UIComponents/Cards/StatsCard.vue'
  import Card from 'src/components/UIComponents/Cards/Card.vue'
  import LTable from 'src/components/UIComponents/Table.vue'
  import Checkbox from 'src/components/UIComponents/Inputs/Checkbox.vue'
  import axios from 'axios';

  export default {
    components: {
      Checkbox,
      Card,
      LTable,
      ChartCard,
      StatsCard
    },
    data () {
      return {
        data: [300, 50, 100],
        posts: [],
        comments: [],
        errors: [],
        todo: [],
        todoo: [],
        progress: [],
        done: [],
        datetime: '',
        testy: 'hello',
        count: 0,
        todocount: 0,
        sumtodo: 0,
        progresscount: 0,
        sumprogress: 0,
        donecount: 0,
        feedid: 0,
        ApinanA: 0,
        ApinanB: 0,
        ApinanOnTime: 0,
        ApinanDelay: 0,

        editTooltip: 'Edit Task',
        deleteTooltip: 'Remove',
        number:10,
        pieChart: {
          data: {
            labels: ['40%', '20%', '40%'],
            series: [40, 20, 40]
          }
        },
        lineChart: {
          data: {
            labels: ['9:00AM', '12:00AM', '3:00PM', '6:00PM', '9:00PM', '12:00PM', '3:00AM', '6:00AM'],
            series: [
              [287, 385, 490, 492, 554, 586, 698, 695],
              [67, 152, 143, 240, 287, 335, 435, 437],
              [23, 113, 67, 108, 190, 239, 307, 308]
            ]
          },
          options: {
            low: 0,
            high: 800,
            showArea: false,
            height: '245px',
            axisX: {
              showGrid: false
            },
            lineSmooth: true,
            showLine: true,
            showPoint: true,
            fullWidth: true,
            chartPadding: {
              right: 50
            }
          },
          responsiveOptions: [
            ['screen and (max-width: 640px)', {
              axisX: {
                labelInterpolationFnc (value) {
                  return value[0]
                }
              }
            }]
          ]
        },
        barChart: {
          data: {
            labels: ['Jan', 'Feb', 'Mar', 'Apr', 'Mai', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
            series: [
              [542, 443, 320, 780, 553, 453, 326, 434, 568, 610, 756, 895],
              [412, 243, 280, 580, 453, 353, 300, 364, 368, 410, 636, 695]
            ]
          },
          options: {
            seriesBarDistance: 10,
            axisX: {
              showGrid: false
            },
            height: '245px'
          },
          responsiveOptions: [
            ['screen and (max-width: 640px)', {
              seriesBarDistance: 5,
              axisX: {
                labelInterpolationFnc (value) {
                  return value[0]
                }
              }
            }]
          ]
        },
        tableData: {
          data: [
            {title: 'Sign contract for "What are conference organizers afraid of?"', checked: false},
            {title: 'Lines From Great Russian Literature? Or E-mails From My Boss?', checked: true},
            {
              title: 'Flooded: One year later, assessing what was lost and what was found when a ravaging rain swept through metro Detroit',
              checked: true
            },
            {title: 'Create 4 Invisible User Experiences you Never Knew About', checked: false},
            {title: 'Read "Following makes Medium better"', checked: false},
            {title: 'Unfollow 5 enemies from twitter', checked: false}
          ]
        }
      }
    },
    computed: {
      chartData () {
        return {
          labels: [
            'Red',
            'Blue',
            'Yellow'
          ],
          datasets: [{
            data: this.data,
            backgroundColor: [
              '#FF6384',
              '#36A2EB',
              '#FFCE56'
            ]
          }]
        }
      }
    },
    mounted () {
      let that = this
      that.datetime = Date().substr(8, 2)
      setInterval(() => {
        // https://github.com/vuejs/vue/issues/2873
        // Array.prototype.$set/$remove deprecated (use Vue.set or Array.prototype.splice instead)
        this.data.forEach((item, i) => {
          this.data.splice(i, 1, Math.ceil(Math.random() * 1000))
        })
      }, 1024)
    },
    watch () {
      count () {
        this.pieChart.data.series[0] = this.count
      }
    },
    // Fetches posts when the component is created.
    created () {
      let that = this
      axios.get('https://graph.facebook.com/138501810233037?fields=feed&access_token=EAACEdEose0cBALgt8D4eBZCWic2ReVNHj0OHsLIRSWQaoJ6bpiWZAmZCHfAcWFoBbVarYguZAllrtUwb4hEmUZBZAcabrpYwHbe1DJUBZBMigl5pKDSO0M3lGhUflyc2Ox7JMmeqGTNZBPxRZA51YaUwoVMiZCz0ETdgNl3W6Yet5427a4ovZCO7QGiBZBhkpNo3omcZD')
      .then(response => {
        this.posts = response.data
        // console.log(this.posts.feed.data)s
        // let cut = posts => this.posts.filter(this.posts.feed.data.message.substr(0, 5) === '#ToDo')

        this.posts.feed.data.forEach(function (message) {
          if (message.message.substr(0, 5) === '#ToDo') {
            let newmessage = {
              id: message.id,
              name: '',
              msg: message.message.substr(6),
              status: 'ยังไม่ได้ทำ',
              date: '',
              dmy: '',
              ondelay: '',
              dash: ''
            }
            // console.log(comment.id)
            that.todo.push(newmessage)
            that.progress.push(newmessage)
            that.done.push(newmessage)
            that.count++
            that.test = that.count

            // if (that.todo.status === 'กำลังทำ') {
            //   console.log('connect')
            // }

            // console.log(that.test.id)
            // that.todo.push(message.message.substr(6))
            // that.todo.push(message.id)
            // that.feedid = message.id
            // console.log(that.feedid)
          }
        })
      })
      axios.get('https://graph.facebook.com/138501810233037?fields=feed{comments}&access_token=EAACEdEose0cBALgt8D4eBZCWic2ReVNHj0OHsLIRSWQaoJ6bpiWZAmZCHfAcWFoBbVarYguZAllrtUwb4hEmUZBZAcabrpYwHbe1DJUBZBMigl5pKDSO0M3lGhUflyc2Ox7JMmeqGTNZBPxRZA51YaUwoVMiZCz0ETdgNl3W6Yet5427a4ovZCO7QGiBZBhkpNo3omcZD')
      .then(response => {
        this.comments = response.data
        // console.log(this.comments.feed.data[0].comments.data[0].from.name)
        // console.log(this.comments.feed.data[0].comments.data[0].message)
        this.comments.feed.data.forEach(function (comment) {
          // let result = that.todo.find(item => item === comment.fields
          // console.log(result);
          // that.progress.push(result)
          // console.log(comment.id)
          comment.comments.data.forEach(function (progress) {
            // console.log(progress.message);
            // console.log(progress.from.name);ssssssssss

            // comment start
            if (progress.message === '#start') {
              let result = that.todo.find(item => item.id === comment.id)

              result.status = 'กำลังทำ'
              result.date = progress.created_time.substr(8, 2)
              result.dmy = progress.created_time.substr(0, 10)
              result.name = progress.from.name
              that.progresscount++
              that.sumall = (that.progresscount + that.donecount)
              that.sumprogress = that.progresscount - that.donecount

              that.todo.push(result)
              // if (that.todo.name === 'Apinan Singbut') {
              //   that.ApinanA++
              //   console.log(that.ApinanA)
              // }

              // console.log(that.datetime)
              // console.log(that.test.id)

            }
            // End comment start
            if (progress.message === '#end') {
              let result = that.todo.find(item => item.id === comment.id)
              if (result.status === 'กำลังทำ') {


              result.status = 'ทำเสร็จแล้ว'
              result.ondelay = progress.created_time.substr(8, 2)
              if (result.date === result.ondelay) {
                result.dash = 'On time'

              }
              else {
                result.dash = 'Delay'

              }
              // console.log(result.status)
              that.donecount++
              that.todo.push(result)

              // console.log(that.test.id)sssหsss
            }
            }

            let results = that.todo.find(item => item.id === comment.id)
            console.log(results.status)
            if (results.status === 'กำลังทำ' && results.name === 'Apinan Singbut') {
              that.ApinanA++
            }
            if (results.status === 'ทำเสร็จแล้ว' && results.name === 'Apinan Singbut') {
              that.ApinanB++
            }
            if (results.dash === 'On time' && results.name === 'Apinan Singbut') {
              that.ApinanOnTime++
            }
            if (results.dash === 'Delay' && results.name === 'Apinan Singbut') {
              that.ApinanDelay++
            }

          })
          // console.log(that.progress)
        })
      })
      .catch(e => {
        this.errors.push(e)
      })
    }
  }
</script>
<style>

</style>
