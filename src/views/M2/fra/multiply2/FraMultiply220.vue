<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
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
    localStorage.setItem("lastpage", this.$route.name)
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
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>20.</h1></div>
                        <div class="chapter_title ltr"><h1>Troisième Expédition de la Pêche ’hommes</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

</div>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Luc 5:1-11 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 5:1-11</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Comme J&eacute;sus se trouvait aupr&egrave;s du lac de G&eacute;n&eacute;sareth, et que la foule se pressait autour de lui pour entendre la parole de Dieu,</p>

<p><sup class="versenum">2&nbsp;</sup>il vit au bord du lac deux barques, d&#39;o&ugrave; les p&ecirc;cheurs &eacute;taient descendus pour laver leurs filets.</p>

<p><sup class="versenum">3&nbsp;</sup>Il monta dans l&#39;une de ces barques, qui &eacute;tait &agrave; Simon, et il le pria de s&#39;&eacute;loigner un peu de terre. Puis il s&#39;assit, et de la barque il enseignait la foule.</p>

<p><sup class="versenum">4&nbsp;</sup>Lorsqu&#39;il eut cess&eacute; de parler, il dit &agrave; Simon: Avance en pleine eau, et jetez vos filets pour p&ecirc;cher.</p>

<p><sup class="versenum">5&nbsp;</sup>Simon lui r&eacute;pondit: Ma&icirc;tre, nous avons travaill&eacute; toute la nuit sans rien prendre; mais, sur ta parole, je jetterai le filet.</p>

<p><sup class="versenum">6&nbsp;</sup>L&#39;ayant jet&eacute;, ils prirent une grande quantit&eacute; de poissons, et leur filet se rompait.</p>

<p><sup class="versenum">7&nbsp;</sup>Ils firent signe &agrave; leurs compagnons qui &eacute;taient dans l&#39;autre barque de venir les aider. Ils vinrent et ils remplirent les deux barques, au point qu&#39;elles enfon&ccedil;aient.</p>

<p><sup class="versenum">8&nbsp;</sup>Quand il vit cela, Simon Pierre tomba aux genoux de J&eacute;sus, et dit: Seigneur, retire-toi de moi, parce que je suis un homme p&eacute;cheur.</p>

<p><sup class="versenum">9&nbsp;</sup>Car l&#39;&eacute;pouvante l&#39;avait saisi, lui et tous ceux qui &eacute;taient avec lui, &agrave; cause de la p&ecirc;che qu&#39;ils avaient faite.</p>

<p><sup class="versenum">10&nbsp;</sup>Il en &eacute;tait de m&ecirc;me de Jacques et de Jean, fils de Z&eacute;b&eacute;d&eacute;e, les associ&eacute;s de Simon. Alors J&eacute;sus dit &agrave; Simon: Ne crains point; d&eacute;sormais tu seras p&ecirc;cheur d&#39;hommes.</p>

<p><sup class="versenum">11&nbsp;</sup>Et, ayant ramen&eacute; les barques &agrave; terre, ils laiss&egrave;rent tout, et le suivirent.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/220.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 5:1-11&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<p>Etudiez chaque passage en utilisant les questions de discussion suivantes:</p>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
</ul>

<p>Questions suppl&eacute;mentaires que vous pouvez poser:</p>

<ul>
	<li>Qu&rsquo;est-ce que ses disciples apprennent?</li>
	<li>Qu&rsquo;est-ce que J&eacute;sus est en train de nous montrer au sujet de sa vie et de son minist&egrave;re (ou leadership) ?</li>
	<li>Qu&rsquo;est ce que J&eacute;sus est en train de montrer au sujet du leadership empreint de pi&eacute;t&eacute; ?</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note1Text')"
        id="note1Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>Maintenant, J&eacute;sus fait une campagne dans le lieu de travail de son &eacute;quipe, la barque de Pierre. Il continue de donner une formation sur le tas pour faire d&rsquo;eux des p&ecirc;cheurs d&#39;hommes. J&eacute;sus arrive t&ocirc;t le matin quand les gens venaient acheter du poisson frais de la p&ecirc;che de la nuit. J&eacute;sus profite de l&#39;occasion pour animer une campagne d&rsquo;&eacute;vang&eacute;lisation &laquo;en plein air&raquo;. Il n&#39;essaye pas de rassembler une grande foule, Il va juste o&ugrave; les gens sont. Il se sert d&rsquo;un &eacute;v&eacute;nement local d&eacute;j&agrave; existant et en fait une opportunit&eacute; de faire sa propre p&ecirc;che et de faire former. Il est int&eacute;ressant de voir que Pierre &eacute;tait retourn&eacute; &agrave; la p&ecirc;che. Il luttait probablement avec son engagement &agrave; suivre J&eacute;sus dans la mission. Mais Pierre avait un c&oelig;ur dispos&eacute; &agrave; ob&eacute;ir &agrave; J&eacute;sus. J&eacute;sus a lanc&eacute; un autre d&eacute;fi &agrave; Pierre, il l&rsquo;accepte et laisse tout pour suivre J&eacute;sus &agrave; plein temps.</p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p><span class="tlid-translation translation" lang="fr"><span title="">Pratiquez les comp&eacute;tences n&eacute;cessaires ou les sujets pr&eacute;c&eacute;dents pour vous pr&eacute;parer &agrave; servir les autres:</span></span></p>

<ul>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Pri&egrave;re, soins, partage</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">Gospel</span></span></li>
	<li><span class="tlid-translation translation" lang="fr"><span title="">&Eacute;tudes bibliques fondamentales.</span></span></li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission</h2>

<ul>
	<li>Identifiez 5 personnes de votre Liste de R&eacute;seau envers qui vous prendrez l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez les promesses &laquo; je le ferai d&rsquo;ici quand &raquo; et parlez-en &agrave; votre groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note2Text')"
        id="note2Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la Mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<p>&nbsp;</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Troisième Expédition de la Pêche ’hommes: ', '/content/M2/fra/multiply2/multiply220.html')">
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