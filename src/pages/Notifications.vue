<template>
  <div class="row">
    <div class="col-md-6">
      <card>
        <h4 slot="header">Notifications Customer in queue </h4>
        
        <base-alert type="info" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message">Bob is waitting for chat for about 2 min </span>
        </base-alert>


        <base-alert type="info" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message"> C is waitting for chat for about 2 mins.</span>
        </base-alert>

        <base-alert type="info" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message"> C is waitting for chat for about 2min.</span>
        </base-alert>

        <base-alert type="info" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message"> C is waitting for chat for about 2min.</span>
        </base-alert>

        <base-alert type="warning" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message"> C is waitting for chat for about 8 min.</span>
        </base-alert>

        <base-alert type="danger" dismissible with-icon>
          <span data-notify="icon" class="tim-icons icon-bell-55"></span>
          <span data-notify="message"> C is waitting for chat more than 10.</span>
        </base-alert>
      </card>
    </div>

    
    <div class="col-md-6">
      <card>
        <h4 slot="header">Notifications states</h4>
        <base-alert type="primary" dismissible>
          <span><b> Primary - </b> waiting for about 2 min</span>
        </base-alert>
        <base-alert type="info" dismissible>
          <span><b> Second level - </b> waiting for about 4 min</span>
        </base-alert>
        <base-alert type="success" dismissible>
          <span><b> Third level - </b> waitting for about 6 min </span>
        </base-alert>
        <base-alert type="warning" dismissible>
          <span><b> Fourth level - </b> waitting for about 8 min </span>
        </base-alert>
        <base-alert type="danger" dismissible>
          <span><b> Danger - </b> waitting more than 10 min</span>
        </base-alert>
      </card>
    </div>

    <div class="col-md-12">
      <card>
        <div class="places-buttons">
          <div class="row">
            <div class="col-md-6 ml-auto mr-auto text-center">
              <h4 class="card-title">
                Notifications Places
                <p class="category">Click to view notifications</p>
              </h4>
            </div>
          </div>
          <div class="row">
            <div class="col-lg-8 ml-auto mr-auto">
              <div class="row">
               
                <div class="col-md-12">
                  <base-button type="primary" block @click="notifyVue('top', 'center')">View Notifications</base-button>
                </div>
                
              </div>
            </div>
          </div>
        </div>
      </card>
    </div>
  </div>
</template>
<script>
  import NotificationTemplate from './Notifications/NotificationTemplate';
  import { BaseAlert } from '@/components';

  export default {
    components: {
      BaseAlert
    },
    data() {
      return {
        type: ["", "info", "success", "warning", "danger"],
        notifications: {
          topCenter: false
        }
      };
    },
    methods: {
      notifyVue(verticalAlign, horizontalAlign) {
        const color = Math.floor(Math.random() * 4 + 1);
        this.$notify({
          component: NotificationTemplate,
          icon: "tim-icons icon-bell-55",
          horizontalAlign: horizontalAlign,
          verticalAlign: verticalAlign,
          type: this.type[color],
          timeout: 0
        });
      }
    }
  };
</script>
<style>
</style>
