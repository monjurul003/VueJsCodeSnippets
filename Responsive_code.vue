<!-- Based on the size of the display this row will change the flex direction from row to column-->
<template>
	<v-card>
		<v-row :style="direction">
			<v-col></v-col>	
			<v-col></v-col>	
		</v-row>
	</v-card>
</template>
<script>
	
export default{
	components:{},
	data(){
		return {}
	},
	methods:{}, 
	computed:{
		direction(){
            switch (this.$vuetify.breakpoint.name) {
                case "xs":
                case "sm":
                case "md":
                    return {"flex-direction" : "column"};
                default:
                    return {"flex-direction" : "row"};
            }
        }
	} 
}
</script>