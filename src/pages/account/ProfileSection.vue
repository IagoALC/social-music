<template>
  <q-page>
    <q-card-section class="row">
      <div class="col-sm-2 text-center" :class="$q.screen.lt.sm ? 'full-width' : $q.screen.lt.md ? 'col-md-2' : ''">
        <q-img
          :src="'/user.jpg'"
          style="width: 200px; height: 200px; border-radius: 50%;"
          :style="$q.screen.lt.sm ? 'width: 100px; height: 100px;' : $q.screen.lt.md ? 'width: 100px; height: 100px;' : ''"
        />
      </div>
      <div class="col-sm-9" :class="$q.screen.lt.sm ? 'full-width text-center' : $q.screen.lt.md ? 'col-md-5' : ''">
        <div class="text-h5 text-weight-medium">John Doe</div>
            <div class="text-body2">Rio de janeiro, Brazil</div>
            <div class="text-body2 bg-positive text-white rounded-borders q-py-xs q-px-xl q-my-md" style="display: inline-block;">
              Number of songs: 6
            </div>
            <div class="text-h6 text-weight-medium">About me</div>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus faucibus nisi sit amet est eleifend viverra. Nulla facilisi. Suspendisse potenti. Sed suscipit dolor eget vestibulum consectetur. Nunc vel enim finibus ex cursus ultricies. Etiam sed consectetur arcu. Proin commodo nisl porttitor dolor mollis, interdum pharetra sem lacinia. Sed aliquet orci vel ligula pulvinar sagittis. Cras pulvinar, erat ut malesuada lacinia, magna purus luctus augue, nec gravida erat nisl non ipsum. Proin pretium tempor felis, non tristique orci maximus nec. Fusce quis tristique nibh, ac auctor orci. </p>
      </div>
      <div class="col-sm-1" :class="$q.screen.lt.sm ? 'full-width text-center' : $q.screen.lt.md ? 'col-md-5' : ''">
        <q-btn
          color="white"
          text-color="positive"
          unelevated
          outline
          label="Edit Profile"
          size="sm"
          type="a"
          :to="{ name: 'account-profile' }"
        />
      </div>
    </q-card-section>
  </q-page>
</template>

<script setup>
</script>