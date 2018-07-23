<template>
  <div>
    <div class="section" v-for="section in sections" :key="section.title">
      <div class="container">
        <h1 class="title">{{section.title}}</h1>
        <div class="columns is-centered">
          <div class="column" v-for="portal in section.portals" :key="portal.url">
            <Card :title="portal.title" :url="portal.url" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Card from '@/components/Card'

export default {
  name: 'Home',
  components: {
    Card
  },
  data: function () {
    return {
      sections: [
        {
          title: 'Apartment',
          portals: [
            {
              title: 'Maintenance Request',
              url: 'https://www.ascendatredrocks.com/apartments/co/lakewood/maintenance-request'
            },
            {
              title: 'Pay Rent',
              url: 'https://domuso.com'
            }
          ]
        },
        {
          title: 'Entertainment',
          portals: [
            {
              title: 'Netflix',
              url: 'https://www.netflix.com/browse'
            }
          ]
        }
      ]
    }
  }
}
</script>
