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
                        <div class="chapter_number ltr"><h1>14.</h1></div>
                        <div class="chapter_title ltr"><h1>La Vraie Foi</h1></div>
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
	<li>Lisez ou observez Jean 4:43-54 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 4:43-54</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">43&nbsp;</sup>Apr&egrave;s ces deux jours, J&eacute;sus partit de l&agrave;, pour se rendre en Galil&eacute;e;</p>

<p><sup class="versenum">44&nbsp;</sup>car il avait d&eacute;clar&eacute; lui-m&ecirc;me qu&#39;un proph&egrave;te n&#39;est pas honor&eacute; dans sa propre patrie.</p>

<p><sup class="versenum">45&nbsp;</sup>Lorsqu&#39;il arriva en Galil&eacute;e, il fut bien re&ccedil;u des Galil&eacute;ens, qui avaient vu tout ce qu&#39;il avait fait &agrave; J&eacute;rusalem pendant la f&ecirc;te; car eux aussi &eacute;taient all&eacute;s &agrave; la f&ecirc;te.</p>

<p><sup class="versenum">46&nbsp;</sup>Il retourna donc &agrave; Cana en Galil&eacute;e, o&ugrave; il avait chang&eacute; l&#39;eau en vin. Il y avait &agrave; Caperna&uuml;m un officier du roi, dont le fils &eacute;tait malade.</p>

<p><sup class="versenum">47&nbsp;</sup>Ayant appris que J&eacute;sus &eacute;tait venu de Jud&eacute;e en Galil&eacute;e, il alla vers lui, et le pria de descendre et de gu&eacute;rir son fils, qui &eacute;tait pr&egrave;s de mourir.</p>

<p><sup class="versenum">48&nbsp;</sup>J&eacute;sus lui dit: Si vous ne voyez des miracles et des prodiges, vous ne croyez point.</p>

<p><sup class="versenum">49&nbsp;</sup>L&#39;officier du roi lui dit: Seigneur, descends avant que mon enfant meure.</p>

<p><sup class="versenum">50&nbsp;</sup>Va, lui dit J&eacute;sus, ton fils vit. Et cet homme crut &agrave; la parole que J&eacute;sus lui avait dite, et il s&#39;en alla.</p>

<p><sup class="versenum">51&nbsp;</sup>Comme d&eacute;j&agrave; il descendait, ses serviteurs venant &agrave; sa rencontre, lui apport&egrave;rent cette nouvelle: Ton enfant vit.</p>

<p><sup class="versenum">52&nbsp;</sup>Il leur demanda &agrave; quelle heure il s&#39;&eacute;tait trouv&eacute; mieux; et ils lui dirent: Hier, &agrave; la septi&egrave;me heure, la fi&egrave;vre l&#39;a quitt&eacute;.</p>

<p><sup class="versenum">53&nbsp;</sup>Le p&egrave;re reconnut que c&#39;&eacute;tait &agrave; cette heure-l&agrave; que J&eacute;sus lui avait dit: Ton fils vit. Et il crut, lui et toute sa maison.</p>

<p><sup class="versenum">54&nbsp;</sup>J&eacute;sus fit encore ce second miracle lorsqu&#39;il fut venu de Jud&eacute;e en Galil&eacute;e.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/214.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 4:43-54&nbsp; </button>
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

<p>J&eacute;sus se rend au nord de sa ville natale de Nazareth, dans le district de Galil&eacute;e, et tout le monde s&#39;interroge sur Lui en parlant de sa col&egrave;re au temple. Lorsque que J&eacute;sus a revisit&eacute; Cana, certaines des nouvelles &agrave; son sujet ont atteint un officier du roi d&eacute;sesp&eacute;r&eacute; dans la grande ville de Caperna&uuml;m. Cet officier &eacute;tait tr&egrave;s probablement un Romain qui esp&eacute;rait que J&eacute;sus pourrait gu&eacute;rir son enfant. Jusqu&#39;&agrave; pr&eacute;sent, il semble que J&eacute;sus n&#39;a gu&eacute;ri personne, mais cela n&#39;a pas emp&ecirc;ch&eacute; cet homme de mettre sa foi en J&eacute;sus. Quand J&eacute;sus a promis que son enfant &eacute;tait gu&eacute;ri, l&#39;officier du roi a cru et a ob&eacute;i &agrave; J&eacute;sus. Le r&eacute;sultat fut que son fils fut gu&eacute;ri et toute sa famille crut et fut sauv&eacute;e. La foi, c&rsquo;est prendre J&eacute;sus au mot, Le croire et agir ensuite dans l&#39;ob&eacute;issance.</p>

<p>&nbsp;</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Matthieu 4:17</span>;&nbsp;
<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">17&nbsp;</sup>D&egrave;s ce moment J&eacute;sus commen&ccedil;a &agrave; pr&ecirc;cher, et &agrave; dire: Repentez-vous, car le royaume des cieux est proche.</p>
<!-- end bible --></div>
<span class="popup-link" @click = "popUp('pop2')"> Marc 1:14-15</span>;&nbsp;

<div class="popup invisible" id="pop2"><!-- begin bible -->
<p><sup class="versenum">14&nbsp;</sup>Apr&egrave;s que Jean eut &eacute;t&eacute; livr&eacute;, J&eacute;sus alla dans la Galil&eacute;e, pr&ecirc;chant l&#39;&Eacute;vangile de Dieu.</p>

<p><sup class="versenum">15&nbsp;</sup>Il disait: Le temps est accompli, et le royaume de Dieu est proche. Repentez-vous, et croyez &agrave; la bonne nouvelle.</p>
<!-- end bible --></div>
<span class="popup-link" @click = "popUp('pop3')"> Luc 4:14-1</span>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">14&nbsp;</sup>J&eacute;sus, rev&ecirc;tu de la puissance de l&#39;Esprit, retourna en Galil&eacute;e, et sa renomm&eacute;e se r&eacute;pandit dans tout le pays d&#39;alentour.</p>
<!-- end bible --></div>

</li>
</ul>


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

			<td class="social" @click="share('lesson', 'La Vraie Foi: ', '/content/M2/fra/multiply2/multiply214.html')">
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