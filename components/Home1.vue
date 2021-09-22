<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" sm="4" no-gutters>
        <div
          class="img1border"
          style="border: black 2px solid; height: 100%; width: 100%"
        >
          <img
            class="img1"
            style="width: 100%; height: 100%"
            src="https://static.wixstatic.com/media/nsplsh_426a6f3934746742577a51~mv2_d_3456_4320_s_4_2.jpg/v1/fill/w_635,h_785,al_c,q_85,usm_0.66_1.00_0.01/nsplsh_426a6f3934746742577a51~mv2_d_3456_4320_s_4_2.webp"
            alt=""
          />
        </div>
      </v-col>
      <v-col cols="12" sm="4" style="">
        <div
          class="mx-autoborder"
          style="border: black 2px solid; height: 100%"
        >
          <v-sheet
            v-if="!$vuetify.breakpoint.smAndDown"
            class="mx-auto"
            max-width="244"
            style="margin-top: 30%; margin-left: 25%; text-align: center"
          >
            <v-card-text>
              <h1 style="padding: 10%; font-weight: normal; font-size: 22px">
                Can your Indian Dukaan or Product or Service become part of the
                story to make India shine? Become part of the Dukaan.com
                movement and reach millions of customers.
              </h1>
              <v-btn class="btn" rounded large> Join Us </v-btn>
            </v-card-text>
          </v-sheet>
          <v-sheet
            v-if="$vuetify.breakpoint.smAndDown"
            class="mx-auto"
            max-width="244"
            style="margin-top: 10%; margin-left: 25%; text-align: center"
          >
            <v-card-text>
              <h1 style="padding: 10%; font-weight: normal; font-size: 22px">
                Can your Indian Dukaan or Product or Service become part of the
                story to make India shine? Become part of the Dukaan.com
                movement and reach millions of customers.
              </h1>
              <v-btn class="btn" rounded large> Join Us </v-btn>
            </v-card-text>
          </v-sheet>
          <!-- <v-sheet
            v-if="page in pages"
            :key="page"
            class="mx-auto"
            max-width="244"
            height="1019"
          >
            <v-card-text>
              <h4>{{ page.main }}</h4>
              <h2>{{ page.head }}</h2>
              <h4>{{ page.title }}</h4>
              <br />

              <div class="text">
                {{ page.content }}
              </div>
            </v-card-text>
          </v-sheet> -->
        </div>
      </v-col>
      <v-col cols="12" sm="4">
        <div
          class="img2border"
          style="border: black 2px solid; width: 107%; height: 100%"
        >
          <img
            class="img3"
            style="height: 99%; width: 98%"
            src="https://static.wixstatic.com/media/nsplsh_2eea1fe5f63e486f968d678970916699~mv2.jpg/v1/fill/w_636,h_785,al_c,q_85,usm_0.66_1.00_0.01/nsplsh_2eea1fe5f63e486f968d678970916699~mv2.webp"
            alt=""
          />
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  //   data() {
  //     return {
  //       pages: [
  //         {
  //           main: 'Read the Book',
  //           head: 'Dukaan.com',
  //           title: 'A 25 year journey',
  //           content:
  //             'This is more than a book. Dukaan.com is a LIVE BOOK. It keeps adding pages, as more people join in.It keeps changing, with time, to be relevant to the present - while documenting the past. Whether it be start-ups, companies, movements - you will find them all within the Dukaan.com book. ',
  //         },
  //         {
  //           main: 'Read the Book',
  //           head: 'Dukaan.com',
  //           title: 'A 25 year journey',
  //           content:
  //             'This is more than a book. Dukaan.com is a LIVE BOOK. It keeps adding pages, as more people join in.It keeps changing, with time, to be relevant to the present - while documenting the past. Whether it be start-ups, companies, movements - you will find them all within the Dukaan.com book. ',
  //         },
  //         {
  //           main: 'Read the Book',
  //           head: 'Dukaan.com',
  //           title: 'A 25 year journey',
  //           content:
  //             'This is more than a book. Dukaan.com is a LIVE BOOK. It keeps adding pages, as more people join in.It keeps changing, with time, to be relevant to the present - while documenting the past. Whether it be start-ups, companies, movements - you will find them all within the Dukaan.com book. ',
  //         },
  //         {
  //           main: 'Read the Book',
  //           head: 'Dukaan.com',
  //           title: 'A 25 year journey',
  //           content:
  //             'This is more than a book. Dukaan.com is a LIVE BOOK. It keeps adding pages, as more people join in.It keeps changing, with time, to be relevant to the present - while documenting the past. Whether it be start-ups, companies, movements - you will find them all within the Dukaan.com book. ',
  //         },
  //       ],
  //     }
  //   },
}
</script>

<style scoped>
h1 {
  font-family: sans-serif;
}
.btn {
  background-image: linear-gradient(blue, red);
  color: white;
}
@media only screen and (max-width: 991px) {
  .mx-auto {
  }
}
</style>
