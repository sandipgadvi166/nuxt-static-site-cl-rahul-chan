<template lang="">
    <div class="bg-black py-5 ">
        <h3 class="text-center h4 text-uppercase ">Contact US</h3>
       
          <b-row class="maxWidth">
          <b-col sm="12" lg="6" md="6" xs="12" xlg="6">

           <div class="contact">
           
          <b-container class="contact__form">
             <b-card no-body title="contact us" subtitle=""> 
            <b-form fluid="sm" @submit="onSubmit" @reset="onReset" v-if="show"> 
              <b-form-group
            id="fieldset-1"
            description="Let us know your name."
            label="Enter your Name"
            label-for="input-1"
            required
          
          >
            <b-form-input id="input-1" v-model="name" trim></b-form-input>
          </b-form-group>
          <b-form-group
            id="fieldset-2"
            description="Let us know your number."
            label="Enter your Phone Number"
            label-for="input-2"
            required
          >
            <b-form-input id="input-2" v-model="phone"   trim  type="number" ></b-form-input>
          </b-form-group>
          <b-form-group
          id="email"
          description="Let us know your email ID"
          label="Enter your Email ID"
          required
          >
            <b-form-input id="email" v-model="email" trim type="email" ></b-form-input>
            </b-form-group>

          </b-form-group>
          <b-form-group
          id="email"
          description="Let us know your Message"
          label="Enter your Message"
          required
          >
                    <b-form-textarea  id="textarea"
              v-model="msg"
              placeholder="Enter something..."
              rows="3"
              max-rows="6" ></b-form-textarea>
            </b-form-group>

             <b-button type="submit" variant="info">Submit</b-button>
             <b-button type="reset" variant="danger">Reset</b-button>
          </b-form>
         
          </b-card>

            </b-container>
          </div>
            </b-col>
            <b-col class="address mt-4">
              <h4 class="text-center">Branch Address</h4>
               <b-card class="sticky">
                 <div class="accordion" role="tablist">
    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-1 variant="info">Pune Contact</b-button>
      </b-card-header>
      <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text>
           <p> <fa :icon="['fa','home']"/> Sr.No, PAP J-145, SK Hotel Lane, Bhosari Industrial Estate, Quality Cirle, Pune 411026</p>
           <p>
                <fa :icon="['fa', 'phone']" />
                7619529948 || 
                <fa :icon="['fa', 'phone']" />
                9890038245
              </p>
          </b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>

    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-2 variant="info">Kolhapur Contact</b-button>
      </b-card-header>
      <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
        <b-card-body>
            <b-card-text>
              <p>
              <fa :icon="['fa','home']"/> Plot No 8 CS No 43, Near Athayu hospital, Pune bangalore highway, Ujalaiwadi, Kolhapur 416008
              </p>
              <p>
                <fa :icon="['fa', 'phone']" />
                7619529948 || 
                <fa :icon="['fa', 'phone']" />
                9890038245
              </p>
               </b-card-text>

        </b-card-body>
      </b-collapse>
    </b-card>

    <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-3 variant="info">Ichalgaranji Contact</b-button>
      </b-card-header>
      <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text>
            <p><fa :icon="['fa','home']"/> Satation road, Near Nagarparpalika, Ichalgaranji 24202110.</p>
            <p><fa :icon="['fa','envelope']"/> bpsichalkaranji@gmail.com</p>
            <p><fa :icon="['fa','phone']" /> 9923222550</p>
          </b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>
     <b-card no-body class="mb-1">
      <b-card-header header-tag="header" class="p-1" role="tab">
        <b-button block v-b-toggle.accordion-4 variant="info">Belagavi Contact</b-button>
      </b-card-header>
      <b-collapse id="accordion-4" accordion="my-accordion" role="tabpanel">
        <b-card-body>
          <b-card-text>
            <p><fa :icon="['fa','home']"/> Kadachi Residency, CTS No:4857/31 Plot No:51 3rd Main, 2nd cross, sadhari nagar near anbedkar bhavan, belgavi 590019</p>
            <p><fa :icon="['fa','envelope']"/> bpsichalkaranji@gmail.com</p>
            <p><fa :icon="['fa','phone']" /> 9923222550</p>
          </b-card-text>
        </b-card-body>
      </b-collapse>
    </b-card>
  </div>
                   </b-card>
            </b-col>
          </b-row>
        
        
      </div>
</template>
<script>
export default {
  methods: {
    onSubmit(event) {
      event.preventDefault()
      alert(JSON.stringify(this.form))
    },
    onReset(event) {
      event.preventDefault()
      // Reset our form values
      this.email = ''
      this.name = ''
      this.email = ''
      this.msg = ''
      this.phone = ''
      // Trick to reset/clear native browser form validation state
      this.show = false
      this.$nextTick(() => {
        this.show = true
      })
    },
  },
  data() {
    return {
      name: '',
      phone: '',
      email: '',
      msg: '',
      show: true,
    }
  },
}
</script>
<style lang="">
</style>