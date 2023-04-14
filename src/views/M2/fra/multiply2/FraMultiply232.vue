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
                        <div class="chapter_number ltr"><h1>32.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership et la Foi</h1></div>
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
	<li>Lisez ou observez Marc 4:35-41 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Marc 4:35-41</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">35&nbsp;</sup>Ce m&ecirc;me jour, sur le soir, J&eacute;sus leur dit: Passons &agrave; l&#39;autre bord.</p>

<p><sup class="versenum">36&nbsp;</sup>Apr&egrave;s avoir renvoy&eacute; la foule, ils l&#39;emmen&egrave;rent dans la barque o&ugrave; il se trouvait; il y avait aussi d&#39;autres barques avec lui.</p>

<p><sup class="versenum">37&nbsp;</sup>Il s&#39;&eacute;leva un grand tourbillon, et les flots se jetaient dans la barque, au point qu&#39;elle se remplissait d&eacute;j&agrave;.</p>

<p><sup class="versenum">38&nbsp;</sup>Et lui, il dormait &agrave; la poupe sur le coussin. Ils le r&eacute;veill&egrave;rent, et lui dirent: Ma&icirc;tre, ne t&#39;inqui&egrave;tes-tu pas de ce que nous p&eacute;rissons?</p>

<p><sup class="versenum">39&nbsp;</sup>S&#39;&eacute;tant r&eacute;veill&eacute;, il mena&ccedil;a le vent, et dit &agrave; la mer: Silence! tais-toi! Et le vent cessa, et il y eut un grand calme.</p>

<p><sup class="versenum">40&nbsp;</sup>Puis il leur dit: Pourquoi avez-vous ainsi peur? Comment n&#39;avez-vous point de foi?</p>

<p><sup class="versenum">41&nbsp;</sup>Ils furent saisis d&#39;une grande frayeur, et ils se dirent les uns aux autres: Quel est donc celui-ci, &agrave; qui ob&eacute;issent m&ecirc;me le vent et la mer?</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/232.mp4" type="button" class="external-movie">
         Regardez &nbsp;Marc 4:35-41&nbsp; </button>
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

<p>Comme le mouvement a grandi, J&eacute;sus a eu du mal &agrave; trouver un endroit pour se reposer sans &ecirc;tre d&eacute;rang&eacute;. Il &eacute;tait si fatigu&eacute; qu&#39;il a dormi &agrave; sous une temp&ecirc;te sur le lac! Oui J&eacute;sus est fatigu&eacute; comme nous, Il &eacute;tait pleinement humain et est devenu comme une de Ses propres cr&eacute;ations (H&eacute;breux 2:17). J&eacute;sus a commenc&eacute; &agrave; utiliser le lac de Galil&eacute;e comme un lieu d&#39;&eacute;vasion et de repos avec Ses leaders. Un vent fort et une temp&ecirc;te furieuse ont commenc&eacute; &agrave; faire entrer de l&#39;eau dans le bateau. Les nouveaux leaders ont &eacute;t&eacute; frapp&eacute;s de peur et ont demand&eacute; de l&#39;aide &agrave; J&eacute;sus. Il les a r&eacute;primand&eacute;s pour ne pas avoir la foi. Il ne s&#39;attendait pas &agrave; ce qu&#39;ils calment la temp&ecirc;te eux-m&ecirc;mes, mais Il s&#39;attendait &agrave; ce qu&#39;ils fassent confiance sachant qu&rsquo;Il ne permettrait pas qu&rsquo;il leur arrive un mal.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 8:22-25</span>;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">22&nbsp;</sup>Un jour, J&eacute;sus monta dans une barque avec ses disciples. Il leur dit: Passons de l&#39;autre c&ocirc;t&eacute; du lac. Et ils partirent.</p>

	<p><sup class="versenum">23&nbsp;</sup>Pendant qu&#39;ils naviguaient, J&eacute;sus s&#39;endormit. Un tourbillon fondit sur le lac, la barque se remplissait d&#39;eau, et ils &eacute;taient en p&eacute;ril.</p>

	<p><sup class="versenum">24&nbsp;</sup>Ils s&#39;approch&egrave;rent et le r&eacute;veill&egrave;rent, en disant: Ma&icirc;tre, ma&icirc;tre, nous p&eacute;rissons! S&#39;&eacute;tant r&eacute;veill&eacute;, il mena&ccedil;a le vent et les flots, qui s&#39;apais&egrave;rent, et le calme revint.</p>

	<p><sup class="versenum">25&nbsp;</sup>Puis il leur dit: O&ugrave; est votre foi? Saisis de frayeur et d&#39;&eacute;tonnement, ils se dirent les uns aux autres: Quel est donc celui-ci, qui commande m&ecirc;me au vent et &agrave; l&#39;eau, et &agrave; qui ils ob&eacute;issent?</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> Matthieu 8:18-27</span>

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus, voyant une grande foule autour de lui, donna l&#39;ordre de passer &agrave; l&#39;autre bord.</p>

	<p><sup class="versenum">19&nbsp;</sup>Un scribe s&#39;approcha, et lui dit: Ma&icirc;tre, je te suivrai partout o&ugrave; tu iras.</p>

	<p><sup class="versenum">20&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Les renards ont des tani&egrave;res, et les oiseaux du ciel ont des nids; mais le Fils de l&#39;homme n&#39;a pas o&ugrave; reposer sa t&ecirc;te.</p>

	<p><sup class="versenum">21&nbsp;</sup>Un autre, d&#39;entre les disciples, lui dit: Seigneur, permets-moi d&#39;aller d&#39;abord ensevelir mon p&egrave;re.</p>

	<p><sup class="versenum">22&nbsp;</sup>Mais J&eacute;sus lui r&eacute;pondit: Suis-moi, et laisse les morts ensevelir leurs morts.</p>

	<p><sup class="versenum">23&nbsp;</sup>Il monta dans la barque, et ses disciples le suivirent.</p>

	<p><sup class="versenum">24&nbsp;</sup>Et voici, il s&#39;&eacute;leva sur la mer une si grande temp&ecirc;te que la barque &eacute;tait couverte par les flots. Et lui, il dormait.</p>

	<p><sup class="versenum">25&nbsp;</sup>Les disciples s&#39;&eacute;tant approch&eacute;s le r&eacute;veill&egrave;rent, et dirent: Seigneur, sauve-nous, nous p&eacute;rissons!</p>

	<p><sup class="versenum">26&nbsp;</sup>Il leur dit: Pourquoi avez-vous peur, gens de peu de foi? Alors il se leva, mena&ccedil;a les vents et la mer, et il y eut un grand calme.</p>

	<p><sup class="versenum">27&nbsp;</sup>Ces hommes furent saisis d&#39;&eacute;tonnement: Quel est celui-ci, disaient-ils, &agrave; qui ob&eacute;issent m&ecirc;me les vents et la mer?</p>
	<!-- end bible --></div>
	&nbsp;</li>
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

			<td class="social" @click="share('lesson', 'Leadership et la Foi: ', '/content/M2/fra/multiply2/multiply232.html')">
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