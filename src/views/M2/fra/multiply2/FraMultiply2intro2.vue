<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"
import VueImageZoomer from '@/components/VueImageZoomer.vue'
import '@/assets/styles/vueImageZoomer.css';


export default {
  components: {
    VueImageZoomer
  },
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply2-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<h1>Période 2 Fondement du Ministère</h1>
<div id="showVideoOptions"></div>
  <h2>   
    <div class="zoom-image">
    <vue-image-zoomer
    regular="/images/zoom/sites/mc2/content/M2/fra/multiply2/period2.png" 
    zoom="/images/zoom/sites/mc2/content/M2/fra/multiply2/period2.png" :zoom-amount="3" img-class="img-fluid" alt="Stage of Ministry">
    <img src="@/assets/sites/mc2/content/M2/fra/multiply2/period2.png" img-class="img-fluid" />
    </vue-image-zoomer>
    </div></h2>

<p>Etablir une fondation relationnelle et centr&eacute;e sur Dieu pour faire des disciples.</p>

<ul>
	<li class="nobreak-final-final">Commencement en mi 26 Ap. J.C., jusqu&rsquo;&agrave; environ 30 ans d&rsquo;&acirc;ge, cette p&eacute;riode couvre 18-21 mois, du Bapt&ecirc;me, commencement du minist&egrave;re public, le premiers contact (<span class="popup-link" @click = "popUp('pop1')"> Jean 1 :35-44</span>)&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">35&nbsp;</sup>Le lendemain, Jean &eacute;tait encore l&agrave;, avec deux de ses disciples;</p>

	<p><sup class="versenum">36&nbsp;</sup>et, ayant regard&eacute; J&eacute;sus qui passait, il dit: Voil&agrave; l&#39;Agneau de Dieu.</p>

	<p><sup class="versenum">37&nbsp;</sup>Les deux disciples l&#39;entendirent prononcer ces paroles, et ils suivirent J&eacute;sus.</p>

	<p><sup class="versenum">38&nbsp;</sup>J&eacute;sus se retourna, et voyant qu&#39;ils le suivaient, il leur dit: Que cherchez-vous? Ils lui r&eacute;pondirent: Rabbi (ce qui signifie Ma&icirc;tre), o&ugrave; demeures-tu?</p>

	<p><sup class="versenum">39&nbsp;</sup>Venez, leur dit-il, et voyez. Ils all&egrave;rent, et ils virent o&ugrave; il demeurait; et ils rest&egrave;rent aupr&egrave;s de lui ce jour-l&agrave;. C&#39;&eacute;tait environ la dixi&egrave;me heure.</p>

	<p><sup class="versenum">40&nbsp;</sup>Andr&eacute;, fr&egrave;re de Simon Pierre, &eacute;tait l&#39;un des deux qui avaient entendu les paroles de Jean, et qui avaient suivi J&eacute;sus.</p>

	<p><sup class="versenum">41&nbsp;</sup>Ce fut lui qui rencontra le premier son fr&egrave;re Simon, et il lui dit: Nous avons trouv&eacute; le Messie (ce qui signifie Christ).</p>

	<p><sup class="versenum">42&nbsp;</sup>Et il le conduisit vers J&eacute;sus. J&eacute;sus, l&#39;ayant regard&eacute;, dit: Tu es Simon, fils de Jonas; tu seras appel&eacute; C&eacute;phas (ce qui signifie Pierre).</p>

	<p><sup class="versenum">43&nbsp;</sup>Le lendemain, J&eacute;sus voulut se rendre en Galil&eacute;e, et il rencontra Philippe. Il lui dit: Suis-moi.</p>

	<p><sup class="versenum">44&nbsp;</sup>Philippe &eacute;tait de Bethsa&iuml;da, de la ville d&#39;Andr&eacute; et de Pierre.</p>
	<!-- end bible --></div>
	puis les premiers disciples puis une foule de plus en plus nombreuse (<span class="popup-link" @click = "popUp('pop7')"> Jean 4:1-4</span>

	<div class="popup invisible" id="pop7"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Le Seigneur sut que les pharisiens avaient appris qu&#39;il faisait et baptisait plus de disciples que Jean.</p>

	<p><sup class="versenum">2&nbsp;</sup>Toutefois J&eacute;sus ne baptisait pas lui-m&ecirc;me, mais c&#39;&eacute;taient ses disciples.</p>

	<p><sup class="versenum">3&nbsp;</sup>Alors il quitta la Jud&eacute;e, et retourna en Galil&eacute;e.</p>

	<p><sup class="versenum">4&nbsp;</sup>Comme il fallait qu&#39;il pass&acirc;t par la Samarie,</p>
	<!-- end bible --></div>
	), jusqu&rsquo;&agrave; son premier rejet dans son village natal, Nazareth (<span class="popup-link" @click = "popUp('pop3')"> Luc 4:16-31</span>).

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">16&nbsp;</sup>Il se rendit &agrave; Nazareth, o&ugrave; il avait &eacute;t&eacute; &eacute;lev&eacute;, et, selon sa coutume, il entra dans la synagogue le jour du sabbat. Il se leva pour faire la lecture,</p>

	<p><sup class="versenum">17&nbsp;</sup>et on lui remit le livre du proph&egrave;te &Eacute;sa&iuml;e. L&#39;ayant d&eacute;roul&eacute;, il trouva l&#39;endroit o&ugrave; il &eacute;tait &eacute;crit:</p>

	<p><sup class="versenum">18&nbsp;</sup>L&#39;Esprit du Seigneur est sur moi, Parce qu&#39;il m&#39;a oint pour annoncer une bonne nouvelle aux pauvres; Il m&#39;a envoy&eacute; pour gu&eacute;rir ceux qui ont le coeur bris&eacute;,</p>

	<p><sup class="versenum">19&nbsp;</sup>Pour proclamer aux captifs la d&eacute;livrance, Et aux aveugles le recouvrement de la vue, Pour renvoyer libres les opprim&eacute;s, Pour publier une ann&eacute;e de gr&acirc;ce du Seigneur.</p>

	<p><sup class="versenum">20&nbsp;</sup>Ensuite, il roula le livre, le remit au serviteur, et s&#39;assit. Tous ceux qui se trouvaient dans la synagogue avaient les regards fix&eacute;s sur lui.</p>

	<p><sup class="versenum">21&nbsp;</sup>Alors il commen&ccedil;a &agrave; leur dire: Aujourd&#39;hui cette parole de l&#39;&Eacute;criture, que vous venez d&#39;entendre, est accomplie.</p>

	<p><sup class="versenum">22&nbsp;</sup>Et tous lui rendaient t&eacute;moignage; ils &eacute;taient &eacute;tonn&eacute;s des paroles de gr&acirc;ce qui sortaient de sa bouche, et ils disaient: N&#39;est-ce pas le fils de Joseph?</p>

	<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus leur dit: Sans doute vous m&#39;appliquerez ce proverbe: M&eacute;decin, gu&eacute;ris-toi toi-m&ecirc;me; et vous me direz: Fais ici, dans ta patrie, tout ce que nous avons appris que tu as fait &agrave; Caperna&uuml;m.</p>

	<p><sup class="versenum">24&nbsp;</sup>Mais, ajouta-t-il, je vous le dis en v&eacute;rit&eacute;, aucun proph&egrave;te n&#39;est bien re&ccedil;u dans sa patrie.</p>

	<p><sup class="versenum">25&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;: il y avait plusieurs veuves en Isra&euml;l du temps d&#39;&Eacute;lie, lorsque le ciel fut ferm&eacute; trois ans et six mois et qu&#39;il y eut une grande famine sur toute la terre;</p>

	<p><sup class="versenum">26&nbsp;</sup>et cependant &Eacute;lie ne fut envoy&eacute; vers aucune d&#39;elles, si ce n&#39;est vers une femme veuve, &agrave; Sarepta, dans le pays de Sidon.</p>

	<p><sup class="versenum">27&nbsp;</sup>Il y avait aussi plusieurs l&eacute;preux en Isra&euml;l du temps d&#39;&Eacute;lis&eacute;e, le proph&egrave;te; et cependant aucun d&#39;eux ne fut purifi&eacute;, si ce n&#39;est Naaman le Syrien.</p>

	<p><sup class="versenum">28&nbsp;</sup>Ils furent tous remplis de col&egrave;re dans la synagogue, lorsqu&#39;ils entendirent ces choses.</p>

	<p><sup class="versenum">29&nbsp;</sup>Et s&#39;&eacute;tant lev&eacute;s, ils le chass&egrave;rent de la ville, et le men&egrave;rent jusqu&#39;au sommet de la montagne sur laquelle leur ville &eacute;tait b&acirc;tie, afin de le pr&eacute;cipiter en bas.</p>

	<p><sup class="versenum">30&nbsp;</sup>Mais J&eacute;sus, passant au milieu d&#39;eux, s&#39;en alla.</p>

	<p><sup class="versenum">31&nbsp;</sup>Il descendit &agrave; Caperna&uuml;m, ville de la Galil&eacute;e; et il enseignait, le jour du sabbat.</p>
	<!-- end bible --></div>
	</li>
</ul>

<p>Cette p&eacute;riode voit les fondements du minist&egrave;re pos&eacute;s&nbsp; et un environnement relationnel b&acirc;ti en rassemblant les gens comme des disciples d&rsquo;une fa&ccedil;on nouvelles.</p>

<ul>
	<li class="nobreak-final-final">Au cours de cette phase, le minist&egrave;re de J&eacute;sus a commenc&eacute; &agrave; partir de rien, et a grandi avec le temps et devenu plus large que la taille du minist&egrave;re de Jean Baptiste avant l&rsquo;emprisonnement de ce dernier (<span class="popup-link" @click = "popUp('pop4')"> Jean 4:1-3</span>;&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Le Seigneur sut que les pharisiens avaient appris qu&#39;il faisait et baptisait plus de disciples que Jean.</p>

	<p><sup class="versenum">2&nbsp;</sup>Toutefois J&eacute;sus ne baptisait pas lui-m&ecirc;me, mais c&#39;&eacute;taient ses disciples.</p>

	<p><sup class="versenum">3&nbsp;</sup>Alors il quitta la Jud&eacute;e, et retourna en Galil&eacute;e.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop6')"> Luc 3:19-20</span>;

	<div class="popup invisible" id="pop6"><!-- begin bible -->
	<p><sup class="versenum">19&nbsp;</sup>Mais H&eacute;rode le t&eacute;trarque, &eacute;tant repris par Jean au sujet d&#39;H&eacute;rodias, femme de son fr&egrave;re, et pour toutes les mauvaises actions qu&#39;il avait commises,</p>

	<p><sup class="versenum">20&nbsp;</sup>ajouta encore &agrave; toutes les autres celle d&#39;enfermer Jean dans la prison.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop8')"> Matthieu 4:12</span>).

	<div class="popup invisible" id="pop8"><!-- begin bible -->
	<p><sup class="versenum">12&nbsp;</sup>J&eacute;sus, ayant appris que Jean avait &eacute;t&eacute; livr&eacute;, se retira dans la Galil&eacute;e.</p>
	<!-- end bible --></div>
	</li>
</ul>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Période 2 Fondement du Ministère: ', '/content/M2/fra/multiply2/multiply2intro2.html')">
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

</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->