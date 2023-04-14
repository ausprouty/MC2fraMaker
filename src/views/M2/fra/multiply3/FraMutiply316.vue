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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply3-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>16.</h1></div>
                        <div class="chapter_title ltr"><h1>Saul rencontre Jésus</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p><em>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</em></p>

<ul>
	<li class="nobreak-final-final">(Facultatif) J&eacute;sus-Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re ; qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;. Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus-Christ homme, qui s&rsquo;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. (<span class="popup-link" @click = "popUp('pop1')"> Philippiens 2:11</span>;&nbsp;

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">11&nbsp;</sup>et que toute langue confesse que J&eacute;sus Christ est Seigneur, &agrave; la gloire de Dieu le P&egrave;re.</p>
	<!-- end bible --></div>
	<span class="popup-link" @click = "popUp('pop2')"> 1 Timoth&eacute;e 2:4-6</span>)

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<p><sup class="versenum">4&nbsp;</sup>qui veut que tous les hommes soient sauv&eacute;s et parviennent &agrave; la connaissance de la v&eacute;rit&eacute;.</p>

	<p><sup class="versenum">5&nbsp;</sup>Car il y a un seul Dieu, et aussi un seul m&eacute;diateur entre Dieu et les hommes, J&eacute;sus Christ homme,</p>

	<p><sup class="versenum">6&nbsp;</sup>qui s&#39;est donn&eacute; lui-m&ecirc;me en ran&ccedil;on pour tous. C&#39;est l&agrave; le t&eacute;moignage rendu en son propre temps,</p>
	<!-- end bible --></div>
	</li>
</ul>

</div>

<h2>Soin</h2>

<p><em>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</em></p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la fid&eacute;lit&eacute;</h2>

<p><em>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour.</em></p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Motivation et encouragement</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p><em>Trouvez un moyen de projeter une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux:</em></p>

<ul>
	<li class="indent">un passage qui leur rappelle le c&oelig;ur du P&egrave;re et de la vision final.</li>
	<li>r&eacute;fl&eacute;chir sur des changements intervenus dans leur vie depuis qu&rsquo;ils ont commenc&eacute; &agrave; suivre Christ</li>
	<li>leur rappeler ce que Dieu veut faire &agrave; travers eux</li>
</ul>

<p><strong>Partagez la GRANDE vision</strong> <em>&laquo; une &eacute;glise pour chaque village et communaut&eacute;, l&rsquo;&eacute;vangile pour chaque personne &raquo;.</em></p>

</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><p>+ Contexte</p></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<ul>
	<li>Demandez au groupe de raconter l&rsquo;histoire de la semaine pass&eacute;e.</li>
</ul>

</div>

<h2>Lisez</h2>

<ul>
	<li>Lisez ou observez Actes 9:1-19 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 9:1-19</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Cependant Saul, respirant encore la menace et le meurtre contre les disciples du Seigneur, se rendit chez le souverain sacrificateur,</p>

<p><sup class="versenum">2&nbsp;</sup>et lui demanda des lettres pour les synagogues de Damas, afin que, s&#39;il trouvait des partisans de la nouvelle doctrine, hommes ou femmes, il les amen&acirc;t li&eacute;s &agrave; J&eacute;rusalem.</p>

<p><sup class="versenum">3&nbsp;</sup>Comme il &eacute;tait en chemin, et qu&#39;il approchait de Damas, tout &agrave; coup une lumi&egrave;re venant du ciel resplendit autour de lui.</p>

<p><sup class="versenum">4&nbsp;</sup>Il tomba par terre, et il entendit une voix qui lui disait: Saul, Saul, pourquoi me pers&eacute;cutes-tu?</p>

<p><sup class="versenum">5&nbsp;</sup>Il r&eacute;pondit: Qui es-tu, Seigneur? Et le Seigneur dit: Je suis J&eacute;sus que tu pers&eacute;cutes. Il te serait dur de regimber contre les aiguillons.</p>

<p><sup class="versenum">6&nbsp;</sup>Tremblant et saisi d&#39;effroi, il dit: Seigneur, que veux-tu que je fasse? Et le Seigneur lui dit: L&egrave;ve-toi, entre dans la ville, et on te dira ce que tu dois faire.</p>

<p><sup class="versenum">7&nbsp;</sup>Les hommes qui l&#39;accompagnaient demeur&egrave;rent stup&eacute;faits; ils entendaient bien la voix, mais ils ne voyaient personne.</p>

<p><sup class="versenum">8&nbsp;</sup>Saul se releva de terre, et, quoique ses yeux fussent ouverts, il ne voyait rien; on le prit par la main, et on le conduisit &agrave; Damas.</p>

<p><sup class="versenum">9&nbsp;</sup>Il resta trois jours sans voir, et il ne mangea ni ne but.</p>

<p><sup class="versenum">10&nbsp;</sup>Or, il y avait &agrave; Damas un disciple nomm&eacute; Ananias. Le Seigneur lui dit dans une vision: Ananias! Il r&eacute;pondit: Me voici, Seigneur!</p>

<p><sup class="versenum">11&nbsp;</sup>Et le Seigneur lui dit: L&egrave;ve-toi, va dans la rue qu&#39;on appelle la droite, et cherche, dans la maison de Judas, un nomm&eacute; Saul de Tarse.</p>

<p><sup class="versenum">12&nbsp;</sup>Car il prie, et il a vu en vision un homme du nom d&#39;Ananias, qui entrait, et qui lui imposait les mains, afin qu&#39;il recouvr&acirc;t la vue. Ananias r&eacute;pondit:</p>

<p><sup class="versenum">13&nbsp;</sup>Seigneur, j&#39;ai appris de plusieurs personnes tous les maux que cet homme a faits &agrave; tes saints dans J&eacute;rusalem;</p>

<p><sup class="versenum">14&nbsp;</sup>et il a ici des pouvoirs, de la part des principaux sacrificateurs, pour lier tous ceux qui invoquent ton nom.</p>

<p><sup class="versenum">15&nbsp;</sup>Mais le Seigneur lui dit: Va, car cet homme est un instrument que j&#39;ai choisi, pour porter mon nom devant les nations, devant les rois, et devant les fils d&#39;Isra&euml;l;</p>

<p><sup class="versenum">16&nbsp;</sup>et je lui montrerai tout ce qu&#39;il doit souffrir pour mon nom.</p>

<p><sup class="versenum">17&nbsp;</sup>Ananias sortit; et, lorsqu&#39;il fut arriv&eacute; dans la maison, il imposa les mains &agrave; Saul, en disant: Saul, mon fr&egrave;re, le Seigneur J&eacute;sus, qui t&#39;est apparu sur le chemin par lequel tu venais, m&#39;a envoy&eacute; pour que tu recouvres la vue et que tu sois rempli du Saint Esprit.</p>

<p><sup class="versenum">18&nbsp;</sup>Au m&ecirc;me instant, il tomba de ses yeux comme des &eacute;cailles, et il recouvra la vue. Il se leva, et fut baptis&eacute;;</p>

<p><sup class="versenum">19&nbsp;</sup>et, apr&egrave;s qu&#39;il eut pris de la nourriture, les forces lui revinrent. Saul resta quelques jours avec les disciples qui &eacute;taient &agrave; Damas.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/316.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 9:1-19&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de d&eacute;couverte</h2>

<ul>
	<li>Qu&rsquo;est-ce qui a retenu votre attention ou qu&rsquo;avez-vous aim&eacute; le plus ? Pourquoi ?</li>
	<li>&Agrave; ce niveau de l&rsquo;histoire, qu&rsquo;est-ce qui est nouveau ou est d&eacute;velopp&eacute; ?</li>
	<li>Quel mod&egrave;le a &eacute;t&eacute; donn&eacute; quant &agrave; la vie d&eacute;pendante de l&rsquo;Esprit, faire de disciples ou au leadership ?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire?</li>
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


<p><em>Des questions suppl&eacute;mentaires dont vous pouvez faire usage:</em></p>

<ul>
	<li>Comment les disciples de J&eacute;sus poursuivent-ils Son &oelig;uvre de faire des disciples et d&rsquo;implantation d&rsquo;&eacute;glises ?</li>
	<li>Comment l&rsquo;&eacute;vangile impacte-t-il les gens et la soci&eacute;t&eacute; ?</li>
	<li>Quels &eacute;taient les barri&egrave;res et les obstacles qui ont &eacute;t&eacute; surmont&eacute;s et comment ont-ils &eacute;t&eacute; surmont&eacute;s ?</li>
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


<h2>Lire, raconter et corriger</h2>

<p>Relisez l&rsquo;histoire. Demandez &agrave; quelqu&rsquo;un de raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</p>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Philippe partageait l&rsquo;&eacute;vangile, faisait des disciples et implantait des &eacute;glises. Dans le m&ecirc;me temps, Saul pers&eacute;cutait passionn&eacute;ment les croyants qui avaient quitt&eacute; J&eacute;rusalem. En les traquant dans chaque ville. Il pensait qu&rsquo;en le faisant, il servait Dieu. Saul &eacute;tait m&ecirc;me volontaire pour les poursuivre dans les villes &eacute;trang&egrave;res &agrave; Damas, soit 240 km de J&eacute;rusalem, d&rsquo;environ une semaine de voyage. Le long de son trajet &agrave; Damas, J&eacute;sus pr&icirc;t l&rsquo;initiative de se r&eacute;v&eacute;ler lui-m&ecirc;me &agrave; Saul. Saul est pass&eacute; d&rsquo;un conqu&eacute;rant audacieux et en col&egrave;re qui d&eacute;testait J&eacute;sus &agrave; celui d&rsquo;un aveugle, d&rsquo;une personne humble qui a besoin d&rsquo;&ecirc;tre guid&eacute; par les autres. J&eacute;sus s&rsquo;identifie si bien avec Ses enfants au point de consid&eacute;rer la pers&eacute;cution des croyants comme une pers&eacute;cution contre Lui. Saul a s&rsquo;&eacute;tait rendu compte que, bien qu&rsquo;il f&ucirc;t passionn&eacute; pour Dieu, ses croyances au sujet de Dieu &eacute;taient fausses. J&eacute;sus a apparu &eacute;galement &agrave; Ananias. M&ecirc;me si Ananias avait de doutes &agrave; s&rsquo;approche de Saul, il a fait un part de foi pour ob&eacute;ir &agrave; J&eacute;sus. Le Seigneur a utilis&eacute; Ananias pour gu&eacute;rir Saul et puis pour le baptiser en m&ecirc;me temps. L&agrave; nous voyons un disciple sans une position de leadership baptiser imm&eacute;diatement un nouveau croyant.</p>

<p>Lisez <span class="popup-link" @click = "popUp('pop3')"> Matthieu 28:18-20</span></p>

<div class="popup invisible" id="pop3"><!-- begin bible -->
<p><sup class="versenum">18&nbsp;</sup>J&eacute;sus, s&#39;&eacute;tant approch&eacute;, leur parla ainsi: Tout pouvoir m&#39;a &eacute;t&eacute; donn&eacute; dans le ciel et sur la terre.</p>

<p><sup class="versenum">19&nbsp;</sup>Allez, faites de toutes les nations des disciples, les baptisant au nom du P&egrave;re, du Fils et du Saint Esprit,</p>

<p><sup class="versenum">20&nbsp;</sup>et enseignez-leur &agrave; observer tout ce que je vous ai prescrit. Et voici, je suis avec vous tous les jours, jusqu&#39;&agrave; la fin du monde.</p>

<p>&nbsp;</p>
<!-- end bible --></div>
</div>

<p><em>Pratiquez ici la lib&eacute;ralit&eacute; et la sainte-c&egrave;ne ou dans la section Se pr&eacute;parer pour la mission.</em></p>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se pr&eacute;parer pour la mission</h2></div>
<div class="collapsed" id ="Text4">
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

<h2>Aller en mission</h2>

<ul>
	<li>Identifiez des gens vers qui ou des endroits o&ugrave; vous pouvez prendre l&rsquo;initiative de faire le minist&egrave;re cette semaine.</li>
	<li>&Eacute;crivez des promesses &laquo; Je ferai d&rsquo;ici quand &raquo; et partagez cela avec votre petit groupe.</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note3Text')"
        id="note3Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Prier pour la mission</h2>

<p>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider &agrave; &ecirc;tre fid&egrave;les et de nous utiliser &agrave; initier un mouvement de faiseurs de disciples.</p>

<h2>B&eacute;n&eacute;diction (facultatif)</h2>
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

			<td class="social" @click="share('lesson', 'Saul rencontre Jésus: ', '/content/M2/fra/multiply3/mutiply316.html')">
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