<script>
  export let size = 80;
  export let opacity = 0.1;
</script>

<svg
  width={size}
  height={size}
  viewBox="0 0 120 120"
  fill="none"
  style="opacity:{opacity}"
>
  <!-- board -->
  <rect x="10" y="10" width="100" height="100" rx="12" fill="currentColor"/>

  <!-- traces -->


  <!-- chips -->
  <rect x="45" y="45" width="30" height="30" rx="3" fill="white"/>
  <rect x="52" y="52" width="16" height="16" rx="2" fill="currentColor"/>

  <!-- components -->
  <circle cx="28" cy="28" r="5" fill="white"/>
  <circle cx="92" cy="28" r="5" fill="white"/>
  <circle cx="28" cy="92" r="5" fill="white"/>
  <circle cx="92" cy="92" r="5" fill="white"/>

  <!-- pins -->
  <path
    d="M45 50 H35 M45 60 H35 M45 70 H35
       M75 50 H85 M75 60 H85 M75 70 H85"
    stroke="white"
    stroke-width="2"
  />
</svg>