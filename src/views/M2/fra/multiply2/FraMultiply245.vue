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
                        <div class="chapter_number ltr"><h1>45.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership c’est l’intendance</h1></div>
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
	<li>Lisez ou observez Luc 19:1-27 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 19:1-27</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>J&eacute;sus, &eacute;tant entr&eacute; dans J&eacute;richo, traversait la ville.</p>

<p><sup class="versenum">2&nbsp;</sup>Et voici, un homme riche, appel&eacute; Zach&eacute;e, chef des publicains, cherchait &agrave; voir qui &eacute;tait J&eacute;sus;</p>

<p><sup class="versenum">3&nbsp;</sup>mais il ne pouvait y parvenir, &agrave; cause de la foule, car il &eacute;tait de petite taille.</p>

<p><sup class="versenum">4&nbsp;</sup>Il courut en avant, et monta sur un sycomore pour le voir, parce qu&#39;il devait passer par l&agrave;.</p>

<p><sup class="versenum">5&nbsp;</sup>Lorsque J&eacute;sus fut arriv&eacute; &agrave; cet endroit, il leva les yeux et lui dit: Zach&eacute;e, h&acirc;te-toi de descendre; car il faut que je demeure aujourd&#39;hui dans ta maison.</p>

<p><sup class="versenum">6&nbsp;</sup>Zach&eacute;e se h&acirc;ta de descendre, et le re&ccedil;ut avec joie.</p>

<p><sup class="versenum">7&nbsp;</sup>Voyant cela, tous murmuraient, et disaient: Il est all&eacute; loger chez un homme p&eacute;cheur.</p>

<p><sup class="versenum">8&nbsp;</sup>Mais Zach&eacute;e, se tenant devant le Seigneur, lui dit: Voici, Seigneur, je donne aux pauvres la moiti&eacute; de mes biens, et, si j&#39;ai fait tort de quelque chose &agrave; quelqu&#39;un, je lui rends le quadruple.</p>

<p><sup class="versenum">9&nbsp;</sup>J&eacute;sus lui dit: Le salut est entr&eacute; aujourd&#39;hui dans cette maison, parce que celui-ci est aussi un fils d&#39;Abraham.</p>

<p><sup class="versenum">10&nbsp;</sup>Car le Fils de l&#39;homme est venu chercher et sauver ce qui &eacute;tait perdu.</p>

<p><sup class="versenum">11&nbsp;</sup>Ils &eacute;coutaient ces choses, et J&eacute;sus ajouta une parabole, parce qu&#39;il &eacute;tait pr&egrave;s de J&eacute;rusalem, et qu&#39;on croyait qu&#39;&agrave; l&#39;instant le royaume de Dieu allait para&icirc;tre.</p>

<p><sup class="versenum">12&nbsp;</sup>Il dit donc: Un homme de haute naissance s&#39;en alla dans un pays lointain, pour se faire investir de l&#39;autorit&eacute; royale, et revenir ensuite.</p>

<p><sup class="versenum">13&nbsp;</sup>Il appela dix de ses serviteurs, leur donna dix mines, et leur dit: Faites-les valoir jusqu&#39;&agrave; ce que je revienne.</p>

<p><sup class="versenum">14&nbsp;</sup>Mais ses concitoyens le ha&iuml;ssaient, et ils envoy&egrave;rent une ambassade apr&egrave;s lui, pour dire: Nous ne voulons pas que cet homme r&egrave;gne sur nous.</p>

<p><sup class="versenum">15&nbsp;</sup>Lorsqu&#39;il fut de retour, apr&egrave;s avoir &eacute;t&eacute; investi de l&#39;autorit&eacute; royale, il fit appeler aupr&egrave;s de lui les serviteurs auxquels il avait donn&eacute; l&#39;argent, afin de conna&icirc;tre comment chacun l&#39;avait fait valoir.</p>

<p><sup class="versenum">16&nbsp;</sup>Le premier vint, et dit: Seigneur, ta mine a rapport&eacute; dix mines.</p>

<p><sup class="versenum">17&nbsp;</sup>Il lui dit: C&#39;est bien, bon serviteur; parce que tu as &eacute;t&eacute; fid&egrave;le en peu de chose, re&ccedil;ois le gouvernement de dix villes.</p>

<p><sup class="versenum">18&nbsp;</sup>Le second vint, et dit: Seigneur, ta mine a produit cinq mines.</p>

<p><sup class="versenum">19&nbsp;</sup>Il lui dit: Toi aussi, sois &eacute;tabli sur cinq villes.</p>

<p><sup class="versenum">20&nbsp;</sup>Un autre vint, et dit: Seigneur, voici ta mine, que j&#39;ai gard&eacute;e dans un linge;</p>

<p><sup class="versenum">21&nbsp;</sup>car j&#39;avais peur de toi, parce que tu es un homme s&eacute;v&egrave;re; tu prends ce que tu n&#39;as pas d&eacute;pos&eacute;, et tu moissonnes ce que tu n&#39;as pas sem&eacute;.</p>

<p><sup class="versenum">22&nbsp;</sup>Il lui dit: Je te juge sur tes paroles, m&eacute;chant serviteur; tu savais que je suis un homme s&eacute;v&egrave;re, prenant ce que je n&#39;ai pas d&eacute;pos&eacute;, et moissonnant ce que je n&#39;ai pas sem&eacute;;</p>

<p><sup class="versenum">23&nbsp;</sup>pourquoi donc n&#39;as-tu pas mis mon argent dans une banque, afin qu&#39;&agrave; mon retour je le retirasse avec un int&eacute;r&ecirc;t?</p>

<p><sup class="versenum">24&nbsp;</sup>Puis il dit &agrave; ceux qui &eacute;taient l&agrave;: Otez-lui la mine, et donnez-la &agrave; celui qui a les dix mines.</p>

<p><sup class="versenum">25&nbsp;</sup>Ils lui dirent: Seigneur, il a dix mines. -</p>

<p><sup class="versenum">26&nbsp;</sup>Je vous le dis, on donnera &agrave; celui qui a, mais &agrave; celui qui n&#39;a pas on &ocirc;tera m&ecirc;me ce qu&#39;il a.</p>

<p><sup class="versenum">27&nbsp;</sup>Au reste, amenez ici mes ennemis, qui n&#39;ont pas voulu que je r&eacute;gnasse sur eux, et tuez-les en ma pr&eacute;sence.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/245.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 19:1-27&nbsp; </button>
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

<p>J&eacute;sus a v&eacute;cu ce qu&#39;Il a enseign&eacute;. A J&eacute;richo, J&eacute;sus rencontre un autre homme tr&egrave;s riche mais extr&ecirc;mement impopulaire qui est le chef publicain de la r&eacute;gion pour Rome. J&eacute;sus r&eacute;v&egrave;le que le P&egrave;re veut qu&#39;Il aille &agrave; la maison de Zach&eacute;e. Les gens sont choqu&eacute;s mais Zach&eacute;e est content et le temps pass&eacute; avec J&eacute;sus change son c&oelig;ur. Il re&ccedil;oit le pardon et commence &agrave; changer ses habitudes. Il demande pardon et corrige les choses avec ceux qu&#39;il a l&eacute;s&eacute;s. Alors qu&#39;ils c&eacute;l&egrave;brent la vie chang&eacute;e de Zach&eacute;e, J&eacute;sus enseigne une parabole sur le fait d&#39;&ecirc;tre un intendant de ce que Dieu nous a donn&eacute;. Un jour, nous devrons rendre compte de la fa&ccedil;on dont nous avons utilis&eacute; les choses de Dieu. Nous sommes les intendants des choses mat&eacute;rielles et aussi des choses spirituelles profondes. En tant que vrais disciples de J&eacute;sus, nous r&eacute;alisons que nous ne poss&eacute;dons rien mais que Dieu est le propri&eacute;taire et nous sommes appel&eacute;s &agrave; g&eacute;rer ce qu&#39;il nous confie. Cela implique notre temps, nos paroles, nos pens&eacute;es et nos actions.</p>

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

			<td class="social" @click="share('lesson', 'Leadership c’est l’intendance: ', '/content/M2/fra/multiply2/multiply245.html')">
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