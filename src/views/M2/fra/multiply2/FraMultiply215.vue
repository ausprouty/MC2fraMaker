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
                        <div class="chapter_number ltr"><h1>15.</h1></div>
                        <div class="chapter_title ltr"><h1>Sans la Foi</h1></div>
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
	<li>Lisez ou observez Luc 4:16-30 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 4:16-30</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

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
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/215.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 4:16-30&nbsp; </button>
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

<p>J&eacute;sus est de retour &agrave; Nazareth, enseignant dans la synagogue locale. Ce sont des gens qui l&#39;auraient connu et sa famille depuis qu&#39;il &eacute;tait un petit gar&ccedil;on. Ils voulaient que J&eacute;sus accomplisse une gu&eacute;rison comme il l&#39;avait fait pour le fils de l&rsquo;officier du roi, mais Il savait qu&#39;ils ne croyaient pas en Lui, ils n&#39;avaient aucune foi. Au d&eacute;but, tout le monde a aim&eacute; ce qu&#39;Il partageait mais ensuite les choses ont chang&eacute; quand Il a commenc&eacute; &agrave; parler du plan de Dieu et de ce qu&#39;Il ferait pour les non- Juifs. Dans leurs pr&eacute;jug&eacute;s, ils s&#39;offusqu&egrave;rent et rejet&egrave;rent J&eacute;sus. Ce n&#39;est que lorsque nous vivons dans la foi que nous pourrons voir Dieu faire l&#39;impossible.</p>

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

			<td class="social" @click="share('lesson', 'Sans la Foi: ', '/content/M2/fra/multiply2/multiply215.html')">
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