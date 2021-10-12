<div class="logo">
  <svg version="1.1" viewBox="0 0 128 174" xmlns="http://www.w3.org/2000/svg">
    <g transform="matrix(1,0,0,-1,0,174)">
      <g transform="translate(99.387 44.405)" class="i">
        <path d="m0 0v42.595h28.398v42.595h-85.19v-127.78h42.595c23.525 0 42.595 19.071 42.595 42.595z" />
      </g>
      <g transform="translate(99.387 44.405)" class="i-shim">
        <path d="m0 0v42.595h28.398v42.595h-85.19v-127.78h42.595c23.525 0 42.595 19.071 42.595 42.595z" />
      </g>
      <g transform="translate(127.78 129.59)" class="f">
        <path
          d="m0 0v42.595h-85.189c-23.525 0-42.596-19.071-42.596-42.595v-127.78h42.596v42.595h28.397v42.595h-28.397v42.595z"
        />
      </g>
    </g>
  </svg>
</div>

<style lang="scss">
  .logo {
    all: inherit;
    path {
      fill: #bbb;
    }
    .i path {
      opacity: 0.45;
    }
    .i-shim path {
      opacity: 0.65;
      fill: $color-primary;
      transition: transform 0.5s $transition-default;
      transform: translateX(-75%);
    }
    &:hover .i-shim path {
      transform: translateX(0);
    }
  }
</style>
