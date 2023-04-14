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
                        <div class="chapter_number ltr"><h1>33.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership et les Forteresses</h1></div>
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
	<li>Lisez ou observez Marc 5:1-20 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Marc 5:1-20</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Ils arriv&egrave;rent &agrave; l&#39;autre bord de la mer, dans le pays des Gadar&eacute;niens.</p>

<p><sup class="versenum">2&nbsp;</sup>Aussit&ocirc;t que J&eacute;sus fut hors de la barque, il vint au-devant de lui un homme, sortant des s&eacute;pulcres, et poss&eacute;d&eacute; d&#39;un esprit impur.</p>

<p><sup class="versenum">3&nbsp;</sup>Cet homme avait sa demeure dans les s&eacute;pulcres, et personne ne pouvait plus le lier, m&ecirc;me avec une cha&icirc;ne.</p>

<p><sup class="versenum">4&nbsp;</sup>Car souvent il avait eu les fers aux pieds et avait &eacute;t&eacute; li&eacute; de cha&icirc;nes, mais il avait rompu les cha&icirc;nes et bris&eacute; les fers, et personne n&#39;avait la force de le dompter.</p>

<p><sup class="versenum">5&nbsp;</sup>Il &eacute;tait sans cesse, nuit et jour, dans les s&eacute;pulcres et sur les montagnes, criant, et se meurtrissant avec des pierres.</p>

<p><sup class="versenum">6&nbsp;</sup>Ayant vu J&eacute;sus de loin, il accourut, se prosterna devant lui,</p>

<p><sup class="versenum">7&nbsp;</sup>et s&#39;&eacute;cria d&#39;une voix forte: Qu&#39;y a-t-il entre moi et toi, J&eacute;sus, Fils du Dieu Tr&egrave;s Haut? Je t&#39;en conjure au nom de Dieu, ne me tourmente pas.</p>

<p><sup class="versenum">8&nbsp;</sup>Car J&eacute;sus lui disait: Sors de cet homme, esprit impur!</p>

<p><sup class="versenum">9&nbsp;</sup>Et, il lui demanda: Quel est ton nom? L&eacute;gion est mon nom, lui r&eacute;pondit-il, car nous sommes plusieurs.</p>

<p><sup class="versenum">10&nbsp;</sup>Et il le priait instamment de ne pas les envoyer hors du pays.</p>

<p><sup class="versenum">11&nbsp;</sup>Il y avait l&agrave;, vers la montagne, un grand troupeau de pourceaux qui paissaient.</p>

<p><sup class="versenum">12&nbsp;</sup>Et les d&eacute;mons le pri&egrave;rent, disant: Envoie-nous dans ces pourceaux, afin que nous entrions en eux.</p>

<p><sup class="versenum">13&nbsp;</sup>Il le leur permit. Et les esprits impurs sortirent, entr&egrave;rent dans les pourceaux, et le troupeau se pr&eacute;cipita des pentes escarp&eacute;es dans la mer: il y en avait environ deux mille, et ils se noy&egrave;rent dans la mer.</p>

<p><sup class="versenum">14&nbsp;</sup>Ceux qui les faisaient pa&icirc;tre s&#39;enfuirent, et r&eacute;pandirent la nouvelle dans la ville et dans les campagnes. Les gens all&egrave;rent voir ce qui &eacute;tait arriv&eacute;.</p>

<p><sup class="versenum">15&nbsp;</sup>Ils vinrent aupr&egrave;s de J&eacute;sus, et ils virent le d&eacute;moniaque, celui qui avait eu la l&eacute;gion, assis, v&ecirc;tu, et dans son bon sens; et ils furent saisis de frayeur.</p>

<p><sup class="versenum">16&nbsp;</sup>Ceux qui avaient vu ce qui s&#39;&eacute;tait pass&eacute; leur racont&egrave;rent ce qui &eacute;tait arriv&eacute; au d&eacute;moniaque et aux pourceaux.</p>

<p><sup class="versenum">17&nbsp;</sup>Alors ils se mirent &agrave; supplier J&eacute;sus de quitter leur territoire.</p>

<p><sup class="versenum">18&nbsp;</sup>Comme il montait dans la barque, celui qui avait &eacute;t&eacute; d&eacute;moniaque lui demanda la permission de rester avec lui.</p>

<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus ne le lui permit pas, mais il lui dit: Va dans ta maison, vers les tiens, et raconte-leur tout ce que le Seigneur t&#39;a fait, et comment il a eu piti&eacute; de toi.</p>

<p><sup class="versenum">20&nbsp;</sup>Il s&#39;en alla, et se mit &agrave; publier dans la D&eacute;capole tout ce que J&eacute;sus avait fait pour lui. Et tous furent dans l&#39;&eacute;tonnement.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/233.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 5:1-20&nbsp; </button>
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

<p>J&eacute;sus emm&egrave;ne ses leaders stagiaires hors de leur zone de confort dans la r&eacute;gion des pa&iuml;ens de la D&eacute;capole, de l&#39;autre c&ocirc;t&eacute; du lac. C&#39;est un autre pays et cette r&eacute;gion particuli&egrave;re est connue pour ses t&eacute;n&egrave;bres spirituelles &agrave; cause d&#39;un homme d&eacute;moniaque sauvage et violent qui terrorisait la r&eacute;gion et vivait en exil en marge de la soci&eacute;t&eacute; parmi les tombes. Sur ce &laquo; voyage missionnaire &agrave; l&#39;&eacute;tranger &raquo;, J&eacute;sus mod&egrave;le &agrave; son &eacute;quipe de leadership Son c&oelig;ur pour tous, sa mission dans le monde entier et la r&eacute;alit&eacute; que personne n&#39;est au-dessus de son pouvoir pour sauver. Cet homme semble &ecirc;tre l&rsquo;objet pour lequel le P&egrave;re a conduit J&eacute;sus &agrave; faire ce voyage. Non seulement il est transform&eacute;, mais il devient une personne de paix invraisemblable renvoy&eacute;e &agrave; t&eacute;moigner de J&eacute;sus &agrave; sa famille et &agrave; ses amis. J&eacute;sus transforme la vie d&#39;une personne qui &agrave; son tour devient l&#39;initi&eacute; pour partager l&#39;Evangile dans une toute nouvelle population.</p>

<ul>
	<li>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Luc 8:26-39</span>.</li>
</ul>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">26&nbsp;</sup>Ils abord&egrave;rent dans le pays des G&eacute;ras&eacute;niens, qui est vis-&agrave;-vis de la Galil&eacute;e.</p>

<p><sup class="versenum">27&nbsp;</sup>Lorsque J&eacute;sus fut descendu &agrave; terre, il vint au-devant de lui un homme de la ville, qui &eacute;tait poss&eacute;d&eacute; de plusieurs d&eacute;mons. Depuis longtemps il ne portait point de v&ecirc;tement, et avait sa demeure non dans une maison, mais dans les s&eacute;pulcres.</p>

<p><sup class="versenum">28&nbsp;</sup>Ayant vu J&eacute;sus, il poussa un cri, se jeta &agrave; ses pieds, et dit d&#39;une voix forte: Qu&#39;y a-t-il entre moi et toi, J&eacute;sus, Fils du Dieu Tr&egrave;s Haut? Je t&#39;en supplie, ne me tourmente pas.</p>

<p><sup class="versenum">29&nbsp;</sup>Car J&eacute;sus commandait &agrave; l&#39;esprit impur de sortir de cet homme, dont il s&#39;&eacute;tait empar&eacute; depuis longtemps; on le gardait li&eacute; de cha&icirc;nes et les fers aux pieds, mais il rompait les liens, et il &eacute;tait entra&icirc;n&eacute; par le d&eacute;mon dans les d&eacute;serts.</p>

<p><sup class="versenum">30&nbsp;</sup>J&eacute;sus lui demanda: Quel est ton nom? L&eacute;gion, r&eacute;pondit-il. Car plusieurs d&eacute;mons &eacute;taient entr&eacute;s en lui.</p>

<p><sup class="versenum">31&nbsp;</sup>Et ils priaient instamment J&eacute;sus de ne pas leur ordonner d&#39;aller dans l&#39;ab&icirc;me.</p>

<p><sup class="versenum">32&nbsp;</sup>Il y avait l&agrave;, dans la montagne, un grand troupeau de pourceaux qui paissaient. Et les d&eacute;mons suppli&egrave;rent J&eacute;sus de leur permettre d&#39;entrer dans ces pourceaux. Il le leur permit.</p>

<p><sup class="versenum">33&nbsp;</sup>Les d&eacute;mons sortirent de cet homme, entr&egrave;rent dans les pourceaux, et le troupeau se pr&eacute;cipita des pentes escarp&eacute;es dans le lac, et se noya.</p>

<p><sup class="versenum">34&nbsp;</sup>Ceux qui les faisaient pa&icirc;tre, voyant ce qui &eacute;tait arriv&eacute;, s&#39;enfuirent, et r&eacute;pandirent la nouvelle dans la ville et dans les campagnes.</p>

<p><sup class="versenum">35&nbsp;</sup>Les gens all&egrave;rent voir ce qui &eacute;tait arriv&eacute;. Ils vinrent aupr&egrave;s de J&eacute;sus, et ils trouv&egrave;rent l&#39;homme de qui &eacute;taient sortis les d&eacute;mons, assis &agrave; ses pieds, v&ecirc;tu, et dans son bon sens; et ils furent saisis de frayeur.</p>

<p><sup class="versenum">36&nbsp;</sup>Ceux qui avaient vu ce qui s&#39;&eacute;tait pass&eacute; leur racont&egrave;rent comment le d&eacute;moniaque avait &eacute;t&eacute; gu&eacute;ri.</p>

<p><sup class="versenum">37&nbsp;</sup>Tous les habitants du pays des G&eacute;ras&eacute;niens pri&egrave;rent J&eacute;sus de s&#39;&eacute;loigner d&#39;eux, car ils &eacute;taient saisis d&#39;une grande crainte. J&eacute;sus monta dans la barque, et s&#39;en retourna.</p>

<p><sup class="versenum">38&nbsp;</sup>L&#39;homme de qui &eacute;taient sortis les d&eacute;mons lui demandait la permission de rester avec lui. Mais J&eacute;sus le renvoya, en disant:</p>

<p><sup class="versenum">39&nbsp;</sup>Retourne dans ta maison, et raconte tout ce que Dieu t&#39;a fait. Il s&#39;en alla, et publia par toute la ville tout ce que J&eacute;sus avait fait pour lui.</p>
<!-- end bible --></div>
&nbsp;&nbsp;

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

			<td class="social" @click="share('lesson', 'Leadership et les Forteresses: ', '/content/M2/fra/multiply2/multiply233.html')">
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