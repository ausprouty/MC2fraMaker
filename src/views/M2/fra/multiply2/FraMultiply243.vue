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
                        <div class="chapter_number ltr"><h1>43.</h1></div>
                        <div class="chapter_title ltr"><h1>Multiplication du Leadership</h1></div>
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
	<li>Lisez ou observez Luc 10:1-42 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Luc 10</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Apr&egrave;s cela, le Seigneur d&eacute;signa encore soixante-dix autres disciples, et il les envoya deux &agrave; deux devant lui dans toutes les villes et dans tous les lieux o&ugrave; lui-m&ecirc;me devait aller.</p>

<p><sup class="versenum">2&nbsp;</sup>Il leur dit: La moisson est grande, mais il y a peu d&#39;ouvriers. Priez donc le ma&icirc;tre de la moisson d&#39;envoyer des ouvriers dans sa moisson.</p>

<p><sup class="versenum">3&nbsp;</sup>Partez; voici, je vous envoie comme des agneaux au milieu des loups.</p>

<p><sup class="versenum">4&nbsp;</sup>Ne portez ni bourse, ni sac, ni souliers, et ne saluez personne en chemin.</p>

<p><sup class="versenum">5&nbsp;</sup>Dans quelque maison que vous entriez, dites d&#39;abord: Que la paix soit sur cette maison!</p>

<p><sup class="versenum">6&nbsp;</sup>Et s&#39;il se trouve l&agrave; un enfant de paix, votre paix reposera sur lui; sinon, elle reviendra &agrave; vous.</p>

<p><sup class="versenum">7&nbsp;</sup>Demeurez dans cette maison-l&agrave;, mangeant et buvant ce qu&#39;on vous donnera; car l&#39;ouvrier m&eacute;rite son salaire. N&#39;allez pas de maison en maison.</p>

<p><sup class="versenum">8&nbsp;</sup>Dans quelque ville que vous entriez, et o&ugrave; l&#39;on vous recevra, mangez ce qui vous sera pr&eacute;sent&eacute;,</p>

<p><sup class="versenum">9&nbsp;</sup>gu&eacute;rissez les malades qui s&#39;y trouveront, et dites-leur: Le royaume de Dieu s&#39;est approch&eacute; de vous.</p>

<p><sup class="versenum">10&nbsp;</sup>Mais dans quelque ville que vous entriez, et o&ugrave; l&#39;on ne vous recevra pas, allez dans ses rues, et dites:</p>

<p><sup class="versenum">11&nbsp;</sup>Nous secouons contre vous la poussi&egrave;re m&ecirc;me de votre ville qui s&#39;est attach&eacute;e &agrave; nos pieds; sachez cependant que le royaume de Dieu s&#39;est approch&eacute;.</p>

<p><sup class="versenum">12&nbsp;</sup>Je vous dis qu&#39;en ce jour Sodome sera trait&eacute;e moins rigoureusement que cette ville-l&agrave;.</p>

<p><sup class="versenum">13&nbsp;</sup>Malheur &agrave; toi, Chorazin! malheur &agrave; toi, Bethsa&iuml;da! car, si les miracles qui ont &eacute;t&eacute; faits au milieu de vous avaient &eacute;t&eacute; faits dans Tyr et dans Sidon, il y a longtemps qu&#39;elles se seraient repenties, en prenant le sac et la cendre.</p>

<p><sup class="versenum">14&nbsp;</sup>C&#39;est pourquoi, au jour du jugement, Tyr et Sidon seront trait&eacute;es moins rigoureusement que vous.</p>

<p><sup class="versenum">15&nbsp;</sup>Et toi, Caperna&uuml;m, qui as &eacute;t&eacute; &eacute;lev&eacute;e jusqu&#39;au ciel, tu seras abaiss&eacute;e jusqu&#39;au s&eacute;jour des morts.</p>

<p><sup class="versenum">16&nbsp;</sup>Celui qui vous &eacute;coute m&#39;&eacute;coute, et celui qui vous rejette me rejette; et celui qui me rejette rejette celui qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">17&nbsp;</sup>Les soixante-dix revinrent avec joie, disant: Seigneur, les d&eacute;mons m&ecirc;mes nous sont soumis en ton nom.</p>

<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus leur dit: Je voyais Satan tomber du ciel comme un &eacute;clair.</p>

<p><sup class="versenum">19&nbsp;</sup>Voici, je vous ai donn&eacute; le pouvoir de marcher sur les serpents et les scorpions, et sur toute la puissance de l&#39;ennemi; et rien ne pourra vous nuire.</p>

<p><sup class="versenum">20&nbsp;</sup>Cependant, ne vous r&eacute;jouissez pas de ce que les esprits vous sont soumis; mais r&eacute;jouissez-vous de ce que vos noms sont &eacute;crits dans les cieux.</p>

<p><sup class="versenum">21&nbsp;</sup>En ce moment m&ecirc;me, J&eacute;sus tressaillit de joie par le Saint Esprit, et il dit: Je te loue, P&egrave;re, Seigneur du ciel et de la terre, de ce que tu as cach&eacute; ces choses aux sages et aux intelligents, et de ce que tu les as r&eacute;v&eacute;l&eacute;es aux enfants. Oui, P&egrave;re, je te loue de ce que tu l&#39;as voulu ainsi.</p>

<p><sup class="versenum">22&nbsp;</sup>Toutes choses m&#39;ont &eacute;t&eacute; donn&eacute;es par mon P&egrave;re, et personne ne conna&icirc;t qui est le Fils, si ce n&#39;est le P&egrave;re, ni qui est le P&egrave;re, si ce n&#39;est le Fils et celui &agrave; qui le Fils veut le r&eacute;v&eacute;ler.</p>

<p><sup class="versenum">23&nbsp;</sup>Et, se tournant vers les disciples, il leur dit en particulier: Heureux les yeux qui voient ce que vous voyez!</p>

<p><sup class="versenum">24&nbsp;</sup>Car je vous dis que beaucoup de proph&egrave;tes et de rois ont d&eacute;sir&eacute; voir ce que vous voyez, et ne l&#39;ont pas vu, entendre ce que vous entendez, et ne l&#39;ont pas entendu.</p>

<p><sup class="versenum">25&nbsp;</sup>Un docteur de la loi se leva, et dit &agrave; J&eacute;sus, pour l&#39;&eacute;prouver: Ma&icirc;tre, que dois-je faire pour h&eacute;riter la vie &eacute;ternelle?</p>

<p><sup class="versenum">26&nbsp;</sup>J&eacute;sus lui dit: Qu&#39;est-il &eacute;crit dans la loi? Qu&#39;y lis-tu?</p>

<p><sup class="versenum">27&nbsp;</sup>Il r&eacute;pondit: Tu aimeras le Seigneur, ton Dieu, de tout ton coeur, de toute ton &acirc;me, de toute ta force, et de toute ta pens&eacute;e; et ton prochain comme toi-m&ecirc;me.</p>

<p><sup class="versenum">28&nbsp;</sup>Tu as bien r&eacute;pondu, lui dit J&eacute;sus; fais cela, et tu vivras.</p>

<p><sup class="versenum">29&nbsp;</sup>Mais lui, voulant se justifier, dit &agrave; J&eacute;sus: Et qui est mon prochain?</p>

<p><sup class="versenum">30&nbsp;</sup>J&eacute;sus reprit la parole, et dit: Un homme descendait de J&eacute;rusalem &agrave; J&eacute;richo. Il tomba au milieu des brigands, qui le d&eacute;pouill&egrave;rent, le charg&egrave;rent de coups, et s&#39;en all&egrave;rent, le laissant &agrave; demi mort.</p>

<p><sup class="versenum">31&nbsp;</sup>Un sacrificateur, qui par hasard descendait par le m&ecirc;me chemin, ayant vu cet homme, passa outre.</p>

<p><sup class="versenum">32&nbsp;</sup>Un L&eacute;vite, qui arriva aussi dans ce lieu, l&#39;ayant vu, passa outre.</p>

<p><sup class="versenum">33&nbsp;</sup>Mais un Samaritain, qui voyageait, &eacute;tant venu l&agrave;, fut &eacute;mu de compassion lorsqu&#39;il le vit.</p>

<p><sup class="versenum">34&nbsp;</sup>Il s&#39;approcha, et banda ses plaies, en y versant de l&#39;huile et du vin; puis il le mit sur sa propre monture, le conduisit &agrave; une h&ocirc;tellerie, et prit soin de lui.</p>

<p><sup class="versenum">35&nbsp;</sup>Le lendemain, il tira deux deniers, les donna &agrave; l&#39;h&ocirc;te, et dit: Aie soin de lui, et ce que tu d&eacute;penseras de plus, je te le rendrai &agrave; mon retour.</p>

<p><sup class="versenum">36&nbsp;</sup>Lequel de ces trois te semble avoir &eacute;t&eacute; le prochain de celui qui &eacute;tait tomb&eacute; au milieu des brigands?</p>

<p><sup class="versenum">37&nbsp;</sup>C&#39;est celui qui a exerc&eacute; la mis&eacute;ricorde envers lui, r&eacute;pondit le docteur de la loi. Et J&eacute;sus lui dit: Va, et toi, fais de m&ecirc;me.</p>

<p><sup class="versenum">38&nbsp;</sup>Comme J&eacute;sus &eacute;tait en chemin avec ses disciples, il entra dans un village, et une femme, nomm&eacute;e Marthe, le re&ccedil;ut dans sa maison.</p>

<p><sup class="versenum">39&nbsp;</sup>Elle avait une soeur, nomm&eacute;e Marie, qui, s&#39;&eacute;tant assise aux pieds du Seigneur, &eacute;coutait sa parole.</p>

<p><sup class="versenum">40&nbsp;</sup>Marthe, occup&eacute;e &agrave; divers soins domestiques, survint et dit: Seigneur, cela ne te fait-il rien que ma soeur me laisse seule pour servir? Dis-lui donc de m&#39;aider.</p>

<p><sup class="versenum">41&nbsp;</sup>Le Seigneur lui r&eacute;pondit: Marthe, Marthe, tu t&#39;inqui&egrave;tes et tu t&#39;agites pour beaucoup de choses.</p>

<p><sup class="versenum">42&nbsp;</sup>Une seule chose est n&eacute;cessaire. Marie a choisi la bonne part, qui ne lui sera point &ocirc;t&eacute;e.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/243.mp4" type="button" class="external-movie">
         Regardez &nbsp;Luc 10&nbsp; </button>
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

<p>Apr&egrave;s la f&ecirc;te de la d&eacute;dicace, J&eacute;sus se rend de l&#39;autre c&ocirc;t&eacute; du Jourdain o&ugrave; Jean l&#39;avait baptis&eacute; trois ans plus t&ocirc;t. J&eacute;sus le prend comme base pour les prochains mois. Il suscite 70 autres leaders et les nomme comme Il l&rsquo;a fait avec les 12 premiers. Il les instruit et les envoie deux par deux dans tout le district de P&eacute;r&eacute;e. Ceci est une autre restructuration qui lance 35 nouvelles &eacute;quipes en plus de J&eacute;sus avec les douze, totalisant 36 &eacute;quipes itin&eacute;rantes. Tout comme les 12 premiers, ils ont &eacute;t&eacute; envoy&eacute;s sans rien, ce qui les a amen&eacute;s &agrave; d&eacute;pendre du P&egrave;re. Il veut pourvoir &agrave; tout ce dont ils auront besoin. Ils se sont dispers&eacute;s et sont all&eacute;s dans chaque ville, ont trouv&eacute; les maisons de paix, ont partag&eacute; le message du Royaume et ont servi le peuple. Quand ils reviennent, ils sont tellement contents du fait que Dieu les utilise, mais J&eacute;sus leur rappelle que leur joie devrait &ecirc;tre que leurs noms sont &eacute;crits dans le Livre de Vie. J&eacute;sus &eacute;clate de joie de voir le plan fonctionner. La volont&eacute; du P&egrave;re &eacute;tait que J&eacute;sus mourrait sur la croix, mais l&#39;&oelig;uvre du P&egrave;re &eacute;tait que J&eacute;sus ferait des disciples, qui feraient des disciples, qui &agrave; leur tour feraient des disciples.</p>

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

			<td class="social" @click="share('lesson', 'Multiplication du Leadership: ', '/content/M2/fra/multiply2/multiply243.html')">
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