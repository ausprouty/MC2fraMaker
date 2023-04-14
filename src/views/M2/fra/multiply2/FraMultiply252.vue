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
                        <div class="chapter_number ltr"><h1>52.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership Obéissant</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <h2>&nbsp;</h2>

<div class="back">
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
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez [Bible Reference] deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Matthieu 28:16-20</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">16&nbsp;</sup>Les onze disciples all&egrave;rent en Galil&eacute;e, sur la montagne que J&eacute;sus leur avait d&eacute;sign&eacute;e.</p>

<p><sup class="versenum">17&nbsp;</sup>Quand ils le virent, ils se prostern&egrave;rent devant lui. Mais quelques-uns eurent des doutes.</p>

<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus, s&#39;&eacute;tant approch&eacute;, leur parla ainsi: Tout pouvoir m&#39;a &eacute;t&eacute; donn&eacute; dans le ciel et sur la terre.</p>

<p><sup class="versenum">19&nbsp;</sup>Allez, faites de toutes les nations des disciples, les baptisant au nom du P&egrave;re, du Fils et du Saint Esprit,</p>

<p><sup class="versenum">20&nbsp;</sup>et enseignez-leur &agrave; observer tout ce que je vous ai prescrit. Et voici, je suis avec vous tous les jours, jusqu&#39;&agrave; la fin du monde.</p>

<p>&nbsp;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/252.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 28:16-20&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ?</li>
	<li>Qu&rsquo;est ce qui est nouveau ou s&rsquo;est d&eacute;velopp&eacute; &agrave; ce point de l&rsquo;histoire de J&eacute;sus?</li>
	<li>Quelle implication du point de vue de l&rsquo;humanit&eacute; ou de la divinit&eacute; de J&eacute;sus voyez-vous dans ce passage ?</li>
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

<p>Pierre conduit le groupe &agrave; la montagne o&ugrave; J&eacute;sus les rencontre. Ils l&#39;adorent comme le sauveur ressuscit&eacute; du monde. C&#39;est ici que J&eacute;sus r&eacute;sume le travail de sa vie et leur donne un commandement simple - faites des disciples! Toute leur formation les avait pr&eacute;par&eacute;s &agrave; cela. J&eacute;sus dit &laquo;allez&raquo;, ce qui signifie litt&eacute;ralement: &laquo;quand vous traversez la vie, faites des disciples&raquo;. Dans les activit&eacute;s quotidiennes de la vie, nous devrions investir dans la vie des autres. Il dit que cela concerne tout le monde, toutes les cultures, toutes les tribus, toutes les langues. Le mouvement de la formation des disciples devrait couvrir le monde entier et Il promet qu&#39;il sera toujours avec nous lorsque nous ob&eacute;irons &agrave; ce commandement. C&#39;est le style de vie que J&eacute;sus nous demande d&#39;avoir. D&rsquo;une mani&egrave;re Significative, cet &eacute;v&eacute;nement a lieu &laquo; sur une montagne en Galil&eacute;e &raquo; donnant sur le paysage o&ugrave; ils ont &eacute;t&eacute; appel&eacute;s et form&eacute;s pour Sa mission et d&#39;o&ugrave; ils pourraient voir les nations environnantes. La derni&egrave;re apparition de J&eacute;sus serait quelques jours plus tard quand il est mont&eacute; sur la Montagne des Oliviers juste en dehors de J&eacute;rusalem (Actes 1: 1-11) leur rappelant d&#39;attendre d&#39;&ecirc;tre remplis du Saint-Esprit &agrave; travers lequel ils seraient habilit&eacute;s &agrave; poursuivre son &oelig;uvre.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Marc 16:19-20</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">19&nbsp;</sup>Le Seigneur, apr&egrave;s leur avoir parl&eacute;, fut enlev&eacute; au ciel, et il s&#39;assit &agrave; la droite de Dieu.</p>

	<p><sup class="versenum">20&nbsp;</sup>Et ils s&#39;en all&egrave;rent pr&ecirc;cher partout. Le Seigneur travaillait avec eux, et confirmait la parole par les miracles qui l&#39;accompagnaient.</p>

	<p>&nbsp;</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Luc 24:50-53</span>;&nbsp;

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">50&nbsp;</sup>Il les conduisit jusque vers B&eacute;thanie, et, ayant lev&eacute; les mains, il les b&eacute;nit.</p>

	<p><sup class="versenum">51&nbsp;</sup>Pendant qu&#39;il les b&eacute;nissait, il se s&eacute;para d&#39;eux, et fut enlev&eacute; au ciel.</p>

	<p><sup class="versenum">52&nbsp;</sup>Pour eux, apr&egrave;s l&#39;avoir ador&eacute;, ils retourn&egrave;rent &agrave; J&eacute;rusalem avec une grande joie;</p>

	<p><sup class="versenum">53&nbsp;</sup>et ils &eacute;taient continuellement dans le temple, louant et b&eacute;nissant Dieu.</p>

	<p>&nbsp;</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop3')"> Actes 1 :1-11</span>.&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">1 </sup>Th&eacute;ophile, j&#39;ai parl&eacute;, dans mon premier livre, de tout ce que J&eacute;sus a commenc&eacute; de faire et d&#39;enseigner d&egrave;s le commencement</p>

	<p><sup class="versenum">2&nbsp;</sup>jusqu&#39;au jour o&ugrave; il fut enlev&eacute; au ciel, apr&egrave;s avoir donn&eacute; ses ordres, par le Saint Esprit, aux ap&ocirc;tres qu&#39;il avait choisis.</p>

	<p><sup class="versenum">3&nbsp;</sup>Apr&egrave;s qu&#39;il eut souffert, il leur apparut vivant, et leur en donna plusieurs preuves, se montrant &agrave; eux pendant quarante jours, et parlant des choses qui concernent le royaume de Dieu.</p>

	<p><sup class="versenum">4&nbsp;</sup>Comme il se trouvait avec eux, il leur recommanda de ne pas s&#39;&eacute;loigner de J&eacute;rusalem, mais d&#39;attendre ce que le P&egrave;re avait promis, ce que je vous ai annonc&eacute;, leur dit-il;</p>

	<p><sup class="versenum">5&nbsp;</sup>car Jean a baptis&eacute; d&#39;eau, mais vous, dans peu de jours, vous serez baptis&eacute;s du Saint Esprit.</p>

	<p><sup class="versenum">6&nbsp;</sup>Alors les ap&ocirc;tres r&eacute;unis lui demand&egrave;rent: Seigneur, est-ce en ce temps que tu r&eacute;tabliras le royaume d&#39;Isra&euml;l?</p>

	<p><sup class="versenum">7&nbsp;</sup>Il leur r&eacute;pondit: Ce n&#39;est pas &agrave; vous de conna&icirc;tre les temps ou les moments que le P&egrave;re a fix&eacute;s de sa propre autorit&eacute;.</p>

	<p><sup class="versenum">8&nbsp;</sup>Mais vous recevrez une puissance, le Saint Esprit survenant sur vous, et vous serez mes t&eacute;moins &agrave; J&eacute;rusalem, dans toute la Jud&eacute;e, dans la Samarie, et jusqu&#39;aux extr&eacute;mit&eacute;s de la terre.</p>

	<p><sup class="versenum">9&nbsp;</sup>Apr&egrave;s avoir dit cela, il fut &eacute;lev&eacute; pendant qu&#39;ils le regardaient, et une nu&eacute;e le d&eacute;roba &agrave; leurs yeux.</p>

	<p><sup class="versenum">10&nbsp;</sup>Et comme ils avaient les regards fix&eacute;s vers le ciel pendant qu&#39;il s&#39;en allait, voici, deux hommes v&ecirc;tus de blanc leur apparurent,</p>

	<p><sup class="versenum">11&nbsp;</sup>et dirent: Hommes Galil&eacute;ens, pourquoi vous arr&ecirc;tez-vous &agrave; regarder au ciel? Ce J&eacute;sus, qui a &eacute;t&eacute; enlev&eacute; au ciel du milieu de vous, viendra de la m&ecirc;me mani&egrave;re que vous l&#39;avez vu allant au ciel.</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>
</div>

<div class="forward">
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

			<td class="social" @click="share('lesson', 'Leadership Obéissant: ', '/content/M2/fra/multiply2/multiply252.html')">
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