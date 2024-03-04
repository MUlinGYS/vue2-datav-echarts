<template>
  <div class="module-box" style="height: 7%">
    <div style="flex: 0 1 25%">
      <dv-decoration-10 style="height: 5px" />
    </div>
    <div style="flex: 0 1 50%">
      <div style="display: flex">
        <dv-decoration-8 style="height: 50px; flex: 1" />
        <div style="flex: 1; align-self: center; text-align: center">
          <dv-decoration-11 style="height: 60px">智慧 中心大屏</dv-decoration-11>
        </div>
        <dv-decoration-8 :reverse="true" style="height: 50px; flex: 1" />
      </div>
    </div>
    <div style="flex: 0 1 25%">
      <dv-decoration-10
        :reverse="true"
        style="height: 5px; transform: rotateY(180deg)"
      />
    </div>
  </div>
</template>
