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
                        <div class="chapter_number ltr"><h1>48.</h1></div>
                        <div class="chapter_title ltr"><h1>Leadership de Soumission</h1></div>
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
	<li>Lisez ou observez Jean 14:1-31; Matthieu 26:36-46 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 14</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Que votre coeur ne se trouble point. Croyez en Dieu, et croyez en moi.</p>

<p><sup class="versenum">2&nbsp;</sup>Il y a plusieurs demeures dans la maison de mon P&egrave;re. Si cela n&#39;&eacute;tait pas, je vous l&#39;aurais dit. Je vais vous pr&eacute;parer une place.</p>

<p><sup class="versenum">3&nbsp;</sup>Et, lorsque je m&#39;en serai all&eacute;, et que je vous aurai pr&eacute;par&eacute; une place, je reviendrai, et je vous prendrai avec moi, afin que l&agrave; o&ugrave; je suis vous y soyez aussi.</p>

<p><sup class="versenum">4&nbsp;</sup>Vous savez o&ugrave; je vais, et vous en savez le chemin.</p>

<p><sup class="versenum">5&nbsp;</sup>Thomas lui dit: Seigneur, nous ne savons o&ugrave; tu vas; comment pouvons-nous en savoir le chemin?</p>

<p><sup class="versenum">6&nbsp;</sup>J&eacute;sus lui dit: Je suis le chemin, la v&eacute;rit&eacute;, et la vie. Nul ne vient au P&egrave;re que par moi.</p>

<p><sup class="versenum">7&nbsp;</sup>Si vous me connaissiez, vous conna&icirc;triez aussi mon P&egrave;re. Et d&egrave;s maintenant vous le connaissez, et vous l&#39;avez vu.</p>

<p><sup class="versenum">8&nbsp;</sup>Philippe lui dit: Seigneur, montre-nous le P&egrave;re, et cela nous suffit.</p>

<p><sup class="versenum">9&nbsp;</sup>J&eacute;sus lui dit: Il y a si longtemps que je suis avec vous, et tu ne m&#39;as pas connu, Philippe! Celui qui m&#39;a vu a vu le P&egrave;re; comment dis-tu: Montre-nous le P&egrave;re?</p>

<p><sup class="versenum">10&nbsp;</sup>Ne crois-tu pas que je suis dans le P&egrave;re, et que le P&egrave;re est en moi? Les paroles que je vous dis, je ne les dis pas de moi-m&ecirc;me; et le P&egrave;re qui demeure en moi, c&#39;est lui qui fait les oeuvres.</p>

<p><sup class="versenum">11&nbsp;</sup>Croyez-moi, je suis dans le P&egrave;re, et le P&egrave;re est en moi; croyez du moins &agrave; cause de ces oeuvres.</p>

<p><sup class="versenum">12&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, celui qui croit en moi fera aussi les oeuvres que je fais, et il en fera de plus grandes, parce que je m&#39;en vais au P&egrave;re;</p>

<p><sup class="versenum">13&nbsp;</sup>et tout ce que vous demanderez en mon nom, je le ferai, afin que le P&egrave;re soit glorifi&eacute; dans le Fils.</p>

<p><sup class="versenum">14&nbsp;</sup>Si vous demandez quelque chose en mon nom, je le ferai.</p>

<p><sup class="versenum">15&nbsp;</sup>Si vous m&#39;aimez, gardez mes commandements.</p>

<p><sup class="versenum">16&nbsp;</sup>Et moi, je prierai le P&egrave;re, et il vous donnera un autre consolateur, afin qu&#39;il demeure &eacute;ternellement avec vous,</p>

<p><sup class="versenum">17&nbsp;</sup>l&#39;Esprit de v&eacute;rit&eacute;, que le monde ne peut recevoir, parce qu&#39;il ne le voit point et ne le conna&icirc;t point; mais vous, vous le connaissez, car il demeure avec vous, et il sera en vous.</p>

<p><sup class="versenum">18&nbsp;</sup>Je ne vous laisserai pas orphelins, je viendrai &agrave; vous.</p>

<p><sup class="versenum">19&nbsp;</sup>Encore un peu de temps, et le monde ne me verra plus; mais vous, vous me verrez, car je vis, et vous vivrez aussi.</p>

<p><sup class="versenum">20&nbsp;</sup>En ce jour-l&agrave;, vous conna&icirc;trez que je suis en mon P&egrave;re, que vous &ecirc;tes en moi, et que je suis en vous.</p>

<p><sup class="versenum">21&nbsp;</sup>Celui qui a mes commandements et qui les garde, c&#39;est celui qui m&#39;aime; et celui qui m&#39;aime sera aim&eacute; de mon P&egrave;re, je l&#39;aimerai, et je me ferai conna&icirc;tre &agrave; lui.</p>

<p><sup class="versenum">22&nbsp;</sup>Jude, non pas l&#39;Iscariot, lui dit: Seigneur, d&#39;o&ugrave; vient que tu te feras conna&icirc;tre &agrave; nous, et non au monde?</p>

<p><sup class="versenum">23&nbsp;</sup>J&eacute;sus lui r&eacute;pondit: Si quelqu&#39;un m&#39;aime, il gardera ma parole, et mon P&egrave;re l&#39;aimera; nous viendrons &agrave; lui, et nous ferons notre demeure chez lui.</p>

<p><sup class="versenum">24&nbsp;</sup>Celui qui ne m&#39;aime pas ne garde point mes paroles. Et la parole que vous entendez n&#39;est pas de moi, mais du P&egrave;re qui m&#39;a envoy&eacute;.</p>

<p><sup class="versenum">25&nbsp;</sup>Je vous ai dit ces choses pendant que je demeure avec vous.</p>

<p><sup class="versenum">26&nbsp;</sup>Mais le consolateur, l&#39;Esprit Saint, que le P&egrave;re enverra en mon nom, vous enseignera toutes choses, et vous rappellera tout ce que je vous ai dit.</p>

<p><sup class="versenum">27&nbsp;</sup>Je vous laisse la paix, je vous donne ma paix. Je ne vous donne pas comme le monde donne. Que votre coeur ne se trouble point, et ne s&#39;alarme point.</p>

<p><sup class="versenum">28&nbsp;</sup>Vous avez entendu que je vous ai dit: Je m&#39;en vais, et je reviens vers vous. Si vous m&#39;aimiez, vous vous r&eacute;jouiriez de ce que je vais au P&egrave;re; car le P&egrave;re est plus grand que moi.</p>

<p><sup class="versenum">29&nbsp;</sup>Et maintenant je vous ai dit ces choses avant qu&#39;elles arrivent, afin que, lorsqu&#39;elles arriveront, vous croyiez.</p>

<p><sup class="versenum">30&nbsp;</sup>Je ne parlerai plus gu&egrave;re avec vous; car le prince du monde vient. Il n&#39;a rien en moi;</p>

<p><sup class="versenum">31&nbsp;</sup>mais afin que le monde sache que j&#39;aime le P&egrave;re, et que j&#39;agis selon l&#39;ordre que le P&egrave;re m&#39;a donn&eacute;, levez-vous, partons d&#39;ici.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/248.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 14&nbsp; </button>
    <div class="collapsed"></div>

<button id="Button1" type="button" class="collapsible bible">Lire Matthieu 26:36-46</button><div class="collapsed" id ="Text1">
<!-- begin bible -->

<p><sup class="versenum">36&nbsp;</sup>L&agrave;-dessus, J&eacute;sus alla avec eux dans un lieu appel&eacute; Geths&eacute;man&eacute;, et il dit aux disciples: Asseyez-vous ici, pendant que je m&#39;&eacute;loignerai pour prier.</p>

<p><sup class="versenum">37&nbsp;</sup>Il prit avec lui Pierre et les deux fils de Z&eacute;b&eacute;d&eacute;e, et il commen&ccedil;a &agrave; &eacute;prouver de la tristesse et des angoisses.</p>

<p><sup class="versenum">38&nbsp;</sup>Il leur dit alors: Mon &acirc;me est triste jusqu&#39;&agrave; la mort; restez ici, et veillez avec moi.</p>

<p><sup class="versenum">39&nbsp;</sup>Puis, ayant fait quelques pas en avant, il se jeta sur sa face, et pria ainsi: Mon P&egrave;re, s&#39;il est possible, que cette coupe s&#39;&eacute;loigne de moi! Toutefois, non pas ce que je veux, mais ce que tu veux.</p>

<p><sup class="versenum">40&nbsp;</sup>Et il vint vers les disciples, qu&#39;il trouva endormis, et il dit &agrave; Pierre: Vous n&#39;avez donc pu veiller une heure avec moi!</p>

<p><sup class="versenum">41&nbsp;</sup>Veillez et priez, afin que vous ne tombiez pas dans la tentation; l&#39;esprit es bien dispos&eacute;, mais la chair est faible.</p>

<p><sup class="versenum">42&nbsp;</sup>Il s&#39;&eacute;loigna une seconde fois, et pria ainsi: Mon P&egrave;re, s&#39;il n&#39;est pas possible que cette coupe s&#39;&eacute;loigne sans que je la boive, que ta volont&eacute; soit faite!</p>

<p><sup class="versenum">43&nbsp;</sup>Il revint, et les trouva encore endormis; car leurs yeux &eacute;taient appesantis.</p>

<p><sup class="versenum">44&nbsp;</sup>Il les quitta, et, s&#39;&eacute;loignant, il pria pour la troisi&egrave;me fois, r&eacute;p&eacute;tant les m&ecirc;mes paroles.</p>

<p><sup class="versenum">45&nbsp;</sup>Puis il alla vers ses disciples, et leur dit: Vous dormez maintenant, et vous vous reposez! Voici, l&#39;heure est proche, et le Fils de l&#39;homme est livr&eacute; aux mains des p&eacute;cheurs.</p>

<p><sup class="versenum">46&nbsp;</sup>Levez-vous, allons; voici, celui qui me livre s&#39;approche.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply2/248-1.mp4" type="button" class="external-movie">
         Regardez &nbsp;Matthieu 26:36-46&nbsp; </button>
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

<p>J&eacute;sus a pass&eacute; les derni&egrave;res ann&eacute;es &agrave; enseigner aux gens comment vivre dans le Royaume de Dieu et &agrave; quoi ressemble le Royaume de Dieu. Au cours de cette derni&egrave;re soir&eacute;e ensemble, il donne un enseignement suppl&eacute;mentaire sur son d&eacute;part et le don de l&#39;Esprit qui sera fait pour les aider &agrave; vivre selon le Royaume. Il y a encore une certaine confusion au sujet de ce qui va se passer dans les heures &agrave; venir, mais J&eacute;sus clarifie qu&#39;il est Dieu qui s&rsquo;est fait chair. J&eacute;sus est notre mod&egrave;le parfait pour la vie et le minist&egrave;re. Nous comprenons Dieu parce qu&#39;Il s&rsquo;est r&eacute;v&eacute;l&eacute; &agrave; travers la vie de J&eacute;sus. J&eacute;sus a fait Ses &oelig;uvres &agrave; travers le P&egrave;re et nous ferons le m&ecirc;me travail de faiseurs de disciples par la puissance de Son Esprit. J&eacute;sus a &eacute;galement &eacute;tabli un mod&egrave;le de leadership qui se soumet au P&egrave;re et fait Sa volont&eacute; par Son pouvoir. Il leur rappelle les fondements de la d&eacute;pendance du Saint- Esprit, la pri&egrave;re, l&#39;ob&eacute;issance au programme du P&egrave;re au sujet du Royaume, la priorit&eacute; de la Parole de Dieu y compris celles de J&eacute;sus, l&#39;exaltation du P&egrave;re et les relations intentionnelles d&#39;amour et de sacrifice.</p>

<ul>
	<li class="nobreak-final-final">Pour une &eacute;tude approfondie: <span class="popup-link" @click = "popUp('pop1')"> Luc 22:39-46</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">39&nbsp;</sup>Apr&egrave;s &ecirc;tre sorti, il alla, selon sa coutume, &agrave; la montagne des Oliviers. Ses disciples le suivirent.</p>

	<p><sup class="versenum">40&nbsp;</sup>Lorsqu&#39;il fut arriv&eacute; dans ce lieu, il leur dit: Priez, afin que vous ne tombiez pas en tentation.</p>

	<p><sup class="versenum">41&nbsp;</sup>Puis il s&#39;&eacute;loigna d&#39;eux &agrave; la distance d&#39;environ un jet de pierre, et, s&#39;&eacute;tant mis &agrave; genoux, il pria,</p>

	<p><sup class="versenum">42&nbsp;</sup>disant: P&egrave;re, si tu voulais &eacute;loigner de moi cette coupe! Toutefois, que ma volont&eacute; ne se fasse pas, mais la tienne.</p>

	<p><sup class="versenum">43&nbsp;</sup>Alors un ange lui apparut du ciel, pour le fortifier.</p>

	<p><sup class="versenum">44&nbsp;</sup>&Eacute;tant en agonie, il priait plus instamment, et sa sueur devint comme des grumeaux de sang, qui tombaient &agrave; terre.</p>

	<p><sup class="versenum">45&nbsp;</sup>Apr&egrave;s avoir pri&eacute;, il se leva, et vint vers les disciples, qu&#39;il trouva endormis de tristesse,</p>

	<p><sup class="versenum">46&nbsp;</sup>et il leur dit: Pourquoi dormez-vous? Levez-vous et priez, afin que vous ne tombiez pas en tentation.</p>
	<!-- end bible --></div>
	&nbsp;<span class="popup-link" @click = "popUp('pop2')"> Marc 14:32-42</span>.

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">32&nbsp;</sup>Ils all&egrave;rent ensuite dans un lieu appel&eacute; Geths&eacute;man&eacute;, et J&eacute;sus dit &agrave; ses disciples: Asseyez-vous ici, pendant que je prierai.</p>

	<p><sup class="versenum">33&nbsp;</sup>Il prit avec lui Pierre, Jacques et Jean, et il commen&ccedil;a &agrave; &eacute;prouver de la frayeur et des angoisses.</p>

	<p><sup class="versenum">34&nbsp;</sup>Il leur dit: Mon &acirc;me est triste jusqu&#39;&agrave; la mort; restez ici, et veillez.</p>

	<p><sup class="versenum">35&nbsp;</sup>Puis, ayant fait quelques pas en avant, il se jeta contre terre, et pria que, s&#39;il &eacute;tait possible, cette heure s&#39;&eacute;loign&acirc;t de lui.</p>

	<p><sup class="versenum">36&nbsp;</sup>Il disait: Abba, P&egrave;re, toutes choses te sont possibles, &eacute;loigne de moi cette coupe! Toutefois, non pas ce que je veux, mais ce que tu veux.</p>

	<p><sup class="versenum">37&nbsp;</sup>Et il vint vers les disciples, qu&#39;il trouva endormis, et il dit &agrave; Pierre: Simon, tu dors! Tu n&#39;as pu veiller une heure!</p>

	<p><sup class="versenum">38&nbsp;</sup>Veillez et priez, afin que vous ne tombiez pas en tentation; l&#39;esprit est bien dispos&eacute;, mais la chair est faible.</p>

	<p><sup class="versenum">39&nbsp;</sup>Il s&#39;&eacute;loigna de nouveau, et fit la m&ecirc;me pri&egrave;re.</p>

	<p><sup class="versenum">40&nbsp;</sup>Il revint, et les trouva encore endormis; car leurs yeux &eacute;taient appesantis. Ils ne surent que lui r&eacute;pondre.</p>

	<p><sup class="versenum">41&nbsp;</sup>Il revint pour la troisi&egrave;me fois, et leur dit: Dormez maintenant, et reposez-vous! C&#39;est assez! L&#39;heure est venue; voici, le Fils de l&#39;homme est livr&eacute; aux mains des p&eacute;cheurs.</p>

	<p><sup class="versenum">42&nbsp;</sup>Levez-vous, allons; voici, celui qui me livre s&#39;approche.</p>
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

			<td class="social" @click="share('lesson', 'Leadership de Soumission: ', '/content/M2/fra/multiply2/multiply248.html')">
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