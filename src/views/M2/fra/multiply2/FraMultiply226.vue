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
                        <div class="chapter_number ltr"><h1>26.</h1></div>
                        <div class="chapter_title ltr"><h1>Choisir les apprentis leaders</h1></div>
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
	<li>Lisez ou observez Luc 6:12-19 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 6:12-19</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">12&nbsp;</sup>En ce temps-l&agrave;, J&eacute;sus se rendit sur la montagne pour prier, et il passa toute la nuit &agrave; prier Dieu.</p>

<p><sup class="versenum">13&nbsp;</sup>Quand le jour parut, il appela ses disciples, et il en choisit douze, auxquels il donna le nom d&#39;ap&ocirc;tres:</p>

<p><sup class="versenum">14&nbsp;</sup>Simon, qu&#39;il nomma Pierre; Andr&eacute;, son fr&egrave;re; Jacques; Jean; Philippe; Barth&eacute;lemy;</p>

<p><sup class="versenum">15&nbsp;</sup>Matthieu; Thomas; Jacques, fils d&#39;Alph&eacute;e; Simon, appel&eacute; le z&eacute;lote;</p>

<p><sup class="versenum">16&nbsp;</sup>Jude, fils de Jacques; et Judas Iscariot, qui devint tra&icirc;tre.</p>

<p><sup class="versenum">17&nbsp;</sup>Il descendit avec eux, et s&#39;arr&ecirc;ta sur un plateau, o&ugrave; se trouvaient une foule de ses disciples et une multitude de peuple de toute la Jud&eacute;e, de J&eacute;rusalem, et de la contr&eacute;e maritime de Tyr et de Sidon. Ils &eacute;taient venus pour l&#39;entendre, et pour &ecirc;tre gu&eacute;ris de leurs maladies.</p>

<p><sup class="versenum">18&nbsp;</sup>Ceux qui &eacute;taient tourment&eacute;s par des esprits impurs &eacute;taient gu&eacute;ris.</p>

<p><sup class="versenum">19&nbsp;</sup>Et toute la foule cherchait &agrave; le toucher, parce qu&#39;une force sortait de lui et les gu&eacute;rissait tous.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/226.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 6:12-19&nbsp; </button>
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

<p>J&eacute;sus se d&eacute;place vers une nouvelle p&eacute;riode du mouvement. Le minist&egrave;re et l&#39;&eacute;lan grandissaient et les gens de partout en Isra&euml;l croyaient en Lui en tant que Messie. C&#39;est &agrave; ce moment crucial que J&eacute;sus lance un appel &agrave; ses disciples &agrave; se r&eacute;unir. Pendant qu&#39;ils se rassemblent, J&eacute;sus monte sur la montagne pour prier, nous donnant le premier principe du d&eacute;veloppement du leadership - la d&eacute;pendance &agrave; Dieu. Revenu fra&icirc;chement de la pri&egrave;re, J&eacute;sus descend de la montagne &agrave; un endroit plus bas et, de nombreux disciples (peut-&ecirc;tre plus de 100), Il d&eacute;signe publiquement les 12 premiers leaders du mouvement et les appelle &laquo;ap&ocirc;tres&raquo; ou &laquo;envoy&eacute;s&raquo;. C&#39;est le deuxi&egrave;me principe du leadership, la d&eacute;signation publique. Les leaders sont choisis parmi un groupe plus large de disciples qui ont &eacute;t&eacute; form&eacute;s &agrave; p&ecirc;cher des hommes. Il les a choisis pour qu&#39;ils soient avec Lui (d&eacute;veloppement personnel) et pour qu&#39;Il les envoie faire les choses qu&#39;il avait commenc&eacute; &agrave; faire (autorit&eacute; pour le minist&egrave;re).</p>

<p>Etude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Marc 3:13-19</span>.&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">13&nbsp;</sup>Il monta ensuite sur la montagne; il appela ceux qu&#39;il voulut, et ils vinrent aupr&egrave;s de lui.</p>

	<p><sup class="versenum">14&nbsp;</sup>Il en &eacute;tablit douze, pour les avoir avec lui,</p>

	<p><sup class="versenum">15&nbsp;</sup>et pour les envoyer pr&ecirc;cher avec le pouvoir de chasser les d&eacute;mons.</p>

	<p><sup class="versenum">16&nbsp;</sup>Voici les douze qu&#39;il &eacute;tablit: Simon, qu&#39;il nomma Pierre;</p>

	<p><sup class="versenum">17&nbsp;</sup>Jacques, fils de Z&eacute;b&eacute;d&eacute;e, et Jean, fr&egrave;re de Jacques, auxquels il donna le nom de Boanerg&egrave;s, qui signifie fils du tonnerre;</p>

	<p><sup class="versenum">18&nbsp;</sup>Andr&eacute;; Philippe; Barth&eacute;lemy; Matthieu; Thomas; Jacques, fils d&#39;Alph&eacute;e; Thadd&eacute;e; Simon le Cananite;</p>

	<p><sup class="versenum">19&nbsp;</sup>et Judas Iscariot, celui qui livra J&eacute;sus.</p>
	<!-- end bible --></div>
</p>

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

			<td class="social" @click="share('lesson', 'Choisir les apprentis leaders: ', '/content/M2/fra/multiply2/multiply226.html')">
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