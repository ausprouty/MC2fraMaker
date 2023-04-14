<script>
import {useShare} from "@/assets/javascript/share.js"

export default {
  
  methods:{
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    }
  },
  mounted() {
    localStorage.setItem("returnpage", this.$route.name)
  }
}
</script>
<template>
  <!-- sdcard template from mc2 -->
  
  <div class="page_content" dir="ltr">
    <div  class="app-series-header">
    <img src="@/assets/images/standard/header-front.png" class="app-series-header" />
  </div>
    <div>
      
    </div>
    <div>
      <!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('fra-multiply1-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/fra/images/standard/Multiply1.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->
<!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('fra-multiply2-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/fra/images/standard/Multiply2.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->
<!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('fra-multiply3-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/fra/images/standard/Multiply3.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->
<!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('fra-tc-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/fra/images/standard/MessagesTransmissibles.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->

    </div>
    <!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'library: ', '/content/M2/fra/index.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
<!-- end sdcard languageFooterSingle -->

</div>
<!-- end default library -->
</template>
<!--- Created by publishLibrary-->
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->