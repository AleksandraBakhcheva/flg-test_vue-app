<template>
  <div>
    <svg viewBox="0 60 320 320">
      <defs>
        <circle id="circle-clip" cx="50%" cy="50%" r="25%" />
        <clipPath id="avatar-clip">
          <use href="#circle-clip" />
        </clipPath>
      </defs>
      <circle cx="50%" cy="50%" r="50%" fill="white" fill-opacity="0.75">
        <animate
          attributeName="r"
          values="15%;20%;30%;15%;20%;25%;30%;15%"
          dur="2s"
          repeatCount="indefinite"
        />
      </circle>
      <image
        height="50%"
        width="50%"
        x="25%"
        y="25%"
        href="../assets/avatar.jpg"
        clip-path="url(#avatar-clip)"
      />
    </svg>
  </div>
</template>

<script>
export default {
  name: "AvatarView",
};
</script>
