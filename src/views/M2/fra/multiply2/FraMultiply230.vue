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
                        <div class="chapter_number ltr"><h1>30.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership mal compris</h1></div>
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
	<li>Lisez ou observez Luc 7:18-35 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 7:18-35</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">18&nbsp;</sup>Jean fut inform&eacute; de toutes ces choses par ses disciples.</p>

<p><sup class="versenum">19&nbsp;</sup>Il en appela deux, et les envoya vers J&eacute;sus, pour lui dire: Es-tu celui qui doit venir, ou devons-nous en attendre un autre?</p>

<p><sup class="versenum">20&nbsp;</sup>Arriv&eacute;s aupr&egrave;s de J&eacute;sus, ils dirent: Jean Baptiste nous a envoy&eacute;s vers toi, pour dire: Es-tu celui qui doit venir, ou devons-nous en attendre un autre?</p>

<p><sup class="versenum">21&nbsp;</sup>A l&#39;heure m&ecirc;me, J&eacute;sus gu&eacute;rit plusieurs personnes de maladies, d&#39;infirmit&eacute;s, et d&#39;esprits malins, et il rendit la vue &agrave; plusieurs aveugles.</p>

<p><sup class="versenum">22&nbsp;</sup>Et il leur r&eacute;pondit: Allez rapporter &agrave; Jean ce que vous avez vu et entendu: les aveugles voient, les boiteux marchent, les l&eacute;preux sont purifi&eacute;s, les sourds entendent, les morts ressuscitent, la bonne nouvelle est annonc&eacute;e aux pauvres.</p>

<p><sup class="versenum">23&nbsp;</sup>Heureux celui pour qui je ne serai pas une occasion de chute!</p>

<p><sup class="versenum">24&nbsp;</sup>Lorsque les envoy&eacute;s de Jean furent partis, J&eacute;sus se mit &agrave; dire &agrave; la foule, au sujet de Jean: Qu&#39;&ecirc;tes-vous all&eacute;s voir au d&eacute;sert? un roseau agit&eacute; par le vent?</p>

<p><sup class="versenum">25&nbsp;</sup>Mais, qu&#39;&ecirc;tes-vous all&eacute;s voir? un homme v&ecirc;tu d&#39;habits pr&eacute;cieux? Voici, ceux qui portent des habits magnifiques, et qui vivent dans les d&eacute;lices, sont dans les maisons des rois.</p>

<p><sup class="versenum">26&nbsp;</sup>Qu&#39;&ecirc;tes-vous donc all&eacute;s voir? un proph&egrave;te? Oui, vous dis-je, et plus qu&#39;un proph&egrave;te.</p>

<p><sup class="versenum">27&nbsp;</sup>C&#39;est celui dont il est &eacute;crit: Voici, j&#39;envoie mon messager devant ta face, Pour pr&eacute;parer ton chemin devant toi.</p>

<p><sup class="versenum">28&nbsp;</sup>Je vous le dis, parmi ceux qui sont n&eacute;s de femmes, il n&#39;y en a point de plus grand que Jean. Cependant, le plus petit dans le royaume de Dieu est plus grand que lui.</p>

<p><sup class="versenum">29&nbsp;</sup>Et tout le peuple qui l&#39;a entendu et m&ecirc;me les publicains ont justifi&eacute; Dieu, en se faisant baptiser du bapt&ecirc;me de Jean;</p>

<p><sup class="versenum">30&nbsp;</sup>mais les pharisiens et les docteurs de la loi, en ne se faisant pas baptiser par lui, ont rendu nul &agrave; leur &eacute;gard le dessein de Dieu.</p>

<p><sup class="versenum">31&nbsp;</sup>A qui donc comparerai-je les hommes de cette g&eacute;n&eacute;ration, et &agrave; qui ressemblent-ils?</p>

<p><sup class="versenum">32&nbsp;</sup>Ils ressemblent aux enfants assis dans la place publique, et qui, se parlant les uns aux autres, disent: Nous vous avons jou&eacute; de la fl&ucirc;te, et vous n&#39;avez pas dans&eacute;; nous vous avons chant&eacute; des complaintes, et vous n&#39;avez pas pleur&eacute;.</p>

<p><sup class="versenum">33&nbsp;</sup>Car Jean Baptiste est venu, ne mangeant pas de pain et ne buvant pas de vin, et vous dites: Il a un d&eacute;mon.</p>

<p><sup class="versenum">34&nbsp;</sup>Le Fils de l&#39;homme est venu, mangeant et buvant, et vous dites: C&#39;est un mangeur et un buveur, un ami des publicains et des gens de mauvaise vie.</p>

<p><sup class="versenum">35&nbsp;</sup>Mais la sagesse a &eacute;t&eacute; justifi&eacute;e par tous ses enfants.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/230.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 7:18-35&nbsp; </button>
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

<p>J&eacute;sus a souvent &eacute;t&eacute; mal compris en tant que leader. Au cours de cette histoire, il approuve son ami Jean en tant que leader. Jean-Baptiste &eacute;tait assis en prison et avait des doutes au sujet de J&eacute;sus &agrave; faire venir le Royaume de Dieu. Alors il envoya quelques-uns de ses disciples restants pour aller demander cela &agrave; J&eacute;sus. J&eacute;sus renvoie les hommes avec une citation de l&rsquo;Ancien Testament tir&eacute;e d&#39;Isa&iuml;e (qui est le m&ecirc;me qu&#39;Il a utilis&eacute; &agrave; Nazareth) pour faire savoir &agrave; Jean qu&#39;Il faisait les &oelig;uvres du Messie. J&eacute;sus a ensuite fait l&rsquo;&eacute;loge de Jean &agrave; ses disciples comme &eacute;tant le plus grand qui soit n&eacute;. Il a contrast&eacute; ceci avec les choses mauvaises que les gens avaient dites au sujet de John. M&ecirc;me apr&egrave;s avoir observ&eacute; J&eacute;sus pendant plus de deux ans, ils l&#39;ont accus&eacute; d&#39;&ecirc;tre poss&eacute;d&eacute; par un d&eacute;mon, un glouton et un ivrogne. &Ecirc;tre mal compris fait partie du leadership.</p>

<p>Pour une &eacute;tude approfondie <span class="popup-link" @click = "popUp('pop1')"> Matthieu 11:2-19</span>.</p>

<div class="popup invisible" id="pop1"><!-- begin bible -->
<p><sup class="versenum">2&nbsp;</sup>Jean, ayant entendu parler dans sa prison des oeuvres du Christ, lui fit dire par ses disciples:</p>

<p><sup class="versenum">3&nbsp;</sup>Es-tu celui qui doit venir, ou devons-nous en attendre un autre?</p>

<p><sup class="versenum">4&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Allez rapporter &agrave; Jean ce que vous entendez et ce que vous voyez:</p>

<p><sup class="versenum">5&nbsp;</sup>les aveugles voient, les boiteux marchent, les l&eacute;preux sont purifi&eacute;s, les sourds entendent, les morts ressuscitent, et la bonne nouvelle est annonc&eacute;e aux pauvres.</p>

<p><sup class="versenum">6&nbsp;</sup>Heureux celui pour qui je ne serai pas une occasion de chute!</p>

<p><sup class="versenum">7&nbsp;</sup>Comme ils s&#39;en allaient, J&eacute;sus se mit &agrave; dire &agrave; la foule, au sujet de Jean: Qu&#39;&ecirc;tes-vous all&eacute;s voir au d&eacute;sert? un roseau agit&eacute; par le vent?</p>

<p><sup class="versenum">8&nbsp;</sup>Mais, qu&#39;&ecirc;tes-vous all&eacute;s voir? un homme v&ecirc;tu d&#39;habits pr&eacute;cieux? Voici, ceux qui portent des habits pr&eacute;cieux sont dans les maisons des rois.</p>

<p><sup class="versenum">9&nbsp;</sup>Qu&#39;&ecirc;tes-vous donc all&eacute;s voir? un proph&egrave;te? Oui, vous dis-je, et plus qu&#39;un proph&egrave;te.</p>

<p><sup class="versenum">10&nbsp;</sup>Car c&#39;est celui dont il est &eacute;crit: Voici, j&#39;envoie mon messager devant ta face, Pour pr&eacute;parer ton chemin devant toi.</p>

<p><sup class="versenum">11&nbsp;</sup>Je vous le dis en v&eacute;rit&eacute;, parmi ceux qui sont n&eacute;s de femmes, il n&#39;en a point paru de plus grand que Jean Baptiste. Cependant, le plus petit dans le royaume des cieux est plus grand que lui.</p>

<p><sup class="versenum">12&nbsp;</sup>Depuis le temps de Jean Baptiste jusqu&#39;&agrave; pr&eacute;sent, le royaume des cieux est forc&eacute;, et ce sont les violents qui s&#39;en s&#39;emparent.</p>

<p><sup class="versenum">13&nbsp;</sup>Car tous les proph&egrave;tes et la loi ont proph&eacute;tis&eacute; jusqu&#39;&agrave; Jean;</p>

<p><sup class="versenum">14&nbsp;</sup>et, si vous voulez le comprendre, c&#39;est lui qui est l&#39;&Eacute;lie qui devait venir.</p>

<p><sup class="versenum">15&nbsp;</sup>Que celui qui a des oreilles pour entendre entende.</p>

<p><sup class="versenum">16&nbsp;</sup>A qui comparerai-je cette g&eacute;n&eacute;ration? Elle ressemble &agrave; des enfants assis dans des places publiques, et qui, s&#39;adressant &agrave; d&#39;autres enfants,</p>

<p><sup class="versenum">17&nbsp;</sup>disent: Nous vous avons jou&eacute; de la fl&ucirc;te, et vous n&#39;avez pas dans&eacute;; nous avons chant&eacute; des complaintes, et vous ne vous &ecirc;tes pas lament&eacute;s.</p>

<p><sup class="versenum">18&nbsp;</sup>Car Jean est venu, ne mangeant ni ne buvant, et ils disent: Il a un d&eacute;mon.</p>

<p><sup class="versenum">19&nbsp;</sup>Le Fils de l&#39;homme est venu, mangeant et buvant, et ils disent: C&#39;est un mangeur et un buveur, un ami des publicains et des gens de mauvaise vie. Mais la sagesse a &eacute;t&eacute; justifi&eacute;e par ses oeuvres.</p>
<!-- end bible --></div>
&nbsp;

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

			<td class="social" @click="share('lesson', 'Leadership mal compris: ', '/content/M2/fra/multiply2/multiply230.html')">
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