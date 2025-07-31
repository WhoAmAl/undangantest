<!-- src/lib/components/CurvedBackground.svelte -->
<div>
<svg
  class="absolute left-0 top-0 w-full h-full z-10"
  viewBox="0 0 672 1195"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
  style="pointer-events: none;"
>
  <g filter="url(#filter0_d_1222_445)">
    <path
      d="M0 0H672.5C672.5 0 507.155 27.7573 417 79.5C326.845 131.243 289 177 217 262C145 347 102.75 507 82 590C61.25 673 0 1195 0 1195V0Z"
      fill="#FAFAFA"
    />
  </g>
  <defs>
    <filter
      id="filter0_d_1222_445"
      x="-12"
      y="-12"
      width="696.5"
      height="1219"
      filterUnits="userSpaceOnUse"
      color-interpolation-filters="sRGB"
    >
      <feFlood flood-opacity="0" result="BackgroundImageFix" />
      <feColorMatrix
        in="SourceAlpha"
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
        result="hardAlpha"
      />
      <feMorphology
        radius="2"
        operator="dilate"
        in="SourceAlpha"
        result="effect1_dropShadow_1222_445"
      />
      <feOffset />
      <feGaussianBlur stdDeviation="5" />
      <feComposite in2="hardAlpha" operator="out" />
      <feColorMatrix
        type="matrix"
        values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.5 0"
      />
      <feBlend
        mode="normal"
        in2="BackgroundImageFix"
        result="effect1_dropShadow_1222_445"
      />
      <feBlend
        mode="normal"
        in="SourceGraphic"
        in2="effect1_dropShadow_1222_445"
        result="shape"
      />
    </filter>
  </defs>
</svg>
</div>