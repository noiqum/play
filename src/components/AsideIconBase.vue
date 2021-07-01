<template>
  <svg xmlns="http://www.w3.org/2000/svg" 
    :width="width" 
    :height="height" 
    :viewBox="viewBox" 
    :aria-labelledby="iconName"
    :stroke-linejoin="stroke-linejoin"
    :stroke-width="stroke-width"
    :stroke-linecap="stroke-linecap"
    :fill="fill"
    :stroke="stroke"
  >
    <title :id="iconName" lang="en">{{iconName}}</title>
    
      <slot />
    
  </svg>
</template>
<script>
export default {
    name:"AsideIconBase",
  props: {
    fill:{type:String,default:"none"},
    "stroke-linejoin":{type:String,default:"round"} ,
    viewBox: { type: String, default: '0 0 32 32'},
    iconName: { type: String, default: ''},
    width: { type: [Number, String], default: 18 },
    height: {type: [Number, String], default: 18 },
    iconColor: {type: String, default: 'currentColor'},
    "stroke-width":{type:String,default:"1"},
    "stroke-linecap":{type:String,default:"round"},
    stroke:{type:String,default:"currentColor"}
  }
}
</script>