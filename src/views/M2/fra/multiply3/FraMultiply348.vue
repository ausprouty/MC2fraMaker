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
                        <div class="chapter_number ltr"><h1>48.</h1></div>
                        <div class="chapter_title ltr"><h1>Paul présente sa défense devant le gouverneur romain Félix</h1></div>
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
	<li>Lisez ou observez Actes 24:1-27 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 24:1-27</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Cinq jours apr&egrave;s, arriva le souverain sacrificateur Ananias, avec des anciens et un orateur nomm&eacute; Tertulle. Ils port&egrave;rent plainte au gouverneur contre Paul.</p>

<p><sup class="versenum">2&nbsp;</sup>Paul fut appel&eacute;, et Tertulle se mit &agrave; l&#39;accuser, en ces termes:</p>

<p><sup class="versenum">3&nbsp;</sup>Tr&egrave;s excellent F&eacute;lix, tu nous fais jouir d&#39;une paix profonde, et cette nation a obtenu de salutaires r&eacute;formes par tes soins pr&eacute;voyants; c&#39;est ce que nous reconnaissons en tout et partout avec une enti&egrave;re gratitude.</p>

<p><sup class="versenum">4&nbsp;</sup>Mais, pour ne pas te retenir davantage, je te prie d&#39;&eacute;couter, dans ta bont&eacute;, ce que nous avons &agrave; dire en peu de mots.</p>

<p><sup class="versenum">5&nbsp;</sup>Nous avons trouv&eacute; cet homme, qui est une peste, qui excite des divisions parmi tous les Juifs du monde, qui est chef de la secte des Nazar&eacute;ens,</p>

<p><sup class="versenum">6&nbsp;</sup>et qui m&ecirc;me a tent&eacute; de profaner le temple. Et nous l&#39;avons arr&ecirc;t&eacute;. Nous avons voulu le juger selon notre loi;</p>

<p><sup class="versenum">7&nbsp;</sup>mais le tribun Lysias &eacute;tant survenu, l&#39;a arrach&eacute; de nos mains avec une grande violence,</p>

<p><sup class="versenum">8&nbsp;</sup>en ordonnant &agrave; ses accusateurs de venir devant toi. Tu pourras toi-m&ecirc;me, en l&#39;interrogeant, apprendre de lui tout ce dont nous l&#39;accusons.</p>

<p><sup class="versenum">9&nbsp;</sup>Les Juifs se joignirent &agrave; l&#39;accusation, soutenant que les choses &eacute;taient ainsi.</p>

<p><sup class="versenum">10&nbsp;</sup>Apr&egrave;s que le gouverneur lui eut fait signe de parler, Paul r&eacute;pondit: Sachant que, depuis plusieurs ann&eacute;es, tu es juge de cette nation, c&#39;est avec confiance que je prends la parole pour d&eacute;fendre ma cause.</p>

<p><sup class="versenum">11&nbsp;</sup>Il n&#39;y a pas plus de douze jours, tu peux t&#39;en assurer, que je suis mont&eacute; &agrave; J&eacute;rusalem pour adorer.</p>

<p><sup class="versenum">12&nbsp;</sup>On ne m&#39;a trouv&eacute; ni dans le temple, ni dans les synagogues, ni dans la ville, disputant avec quelqu&#39;un, ou provoquant un rassemblement s&eacute;ditieux de la foule.</p>

<p><sup class="versenum">13&nbsp;</sup>Et ils ne sauraient prouver ce dont ils m&#39;accusent maintenant.</p>

<p><sup class="versenum">14&nbsp;</sup>Je t&#39;avoue bien que je sers le Dieu de mes p&egrave;res selon la voie qu&#39;ils appellent une secte, croyant tout ce qui est &eacute;crit dans la loi et dans les proph&egrave;tes,</p>

<p><sup class="versenum">15&nbsp;</sup>et ayant en Dieu cette esp&eacute;rance, comme ils l&#39;ont eux-m&ecirc;mes, qu&#39;il y aura une r&eacute;surrection des justes et des injustes.</p>

<p><sup class="versenum">16&nbsp;</sup>C&#39;est pourquoi je m&#39;efforce d&#39;avoir constamment une conscience sans reproche devant Dieu et devant les hommes.</p>

<p><sup class="versenum">17&nbsp;</sup>Apr&egrave;s une absence de plusieurs ann&eacute;es, je suis venu pour faire des aum&ocirc;nes &agrave; ma nation, et pour pr&eacute;senter des offrandes.</p>

<p><sup class="versenum">18&nbsp;</sup>C&#39;est alors que quelques Juifs d&#39;Asie m&#39;ont trouv&eacute; purifi&eacute; dans le temple, sans attroupement ni tumulte.</p>

<p><sup class="versenum">19&nbsp;</sup>C&#39;&eacute;tait &agrave; eux de para&icirc;tre en ta pr&eacute;sence et de se porter accusateurs, s&#39;ils avaient quelque chose contre moi.</p>

<p><sup class="versenum">20&nbsp;</sup>Ou bien, que ceux-ci d&eacute;clarent de quel crime ils m&#39;ont trouv&eacute; coupable, lorsque j&#39;ai comparu devant le sanh&eacute;drin,</p>

<p><sup class="versenum">21&nbsp;</sup>&agrave; moins que ce ne soit uniquement de ce cri que j&#39;ai fait entendre au milieu d&#39;eux: C&#39;est &agrave; cause de la r&eacute;surrection des morts que je suis aujourd&#39;hui mis en jugement devant vous.</p>

<p><sup class="versenum">22&nbsp;</sup>F&eacute;lix, qui savait assez exactement ce qui concernait cette doctrine, les ajourna, en disant: Quand le tribun Lysias sera venu, j&#39;examinerai votre affaire.</p>

<p><sup class="versenum">23&nbsp;</sup>Et il donna l&#39;ordre au centenier de garder Paul, en lui laissant une certaine libert&eacute;, et en n&#39;emp&ecirc;chant aucun des siens de lui rendre des services.</p>

<p><sup class="versenum">24&nbsp;</sup>Quelques jours apr&egrave;s, F&eacute;lix vint avec Drusille, sa femme, qui &eacute;tait Juive, et il fit appeler Paul. Il l&#39;entendit sur la foi en Christ.</p>

<p><sup class="versenum">25&nbsp;</sup>Mais, comme Paul discourait sur la justice, sur la temp&eacute;rance, et sur le jugement &agrave; venir, F&eacute;lix, effray&eacute;, dit: Pour le moment retire-toi; quand j&#39;en trouverai l&#39;occasion, je te rappellerai.</p>

<p><sup class="versenum">26&nbsp;</sup>Il esp&eacute;rait en m&ecirc;me temps que Paul lui donnerait de l&#39;argent; aussi l&#39;envoyait-il chercher assez fr&eacute;quemment, pour s&#39;entretenir avec lui.</p>

<p><sup class="versenum">27&nbsp;</sup>Deux ans s&#39;&eacute;coul&egrave;rent ainsi, et F&eacute;lix eut pour successeur Porcius Festus. Dans le d&eacute;sir de plaire aux Juifs, F&eacute;lix laissa Paul en prison.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/348.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 24:1-27&nbsp; </button>
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

<p>Les pers&eacute;cuteurs juifs &eacute;taient violents et avaient des pr&eacute;jug&eacute;s. Les Romains &eacute;taient ouverts d&#39;esprit et faisaient tout pour op&eacute;rer dans le respect de la loi et de l&#39;ordre. Paul est pris entre deux puissances: J&eacute;rusalem et Rome, religieuse et civil, hostile et amicale. Bien qu&#39;impuissant et vuln&eacute;rable, il est convaincu que les Romains n&#39;ont aucune plainte contre lui et que les Juifs n&#39;ont aucun dossier juridique &agrave; pr&eacute;senter. Il a &eacute;galement confiance dans la promesse du Seigneur de t&eacute;moigner &agrave; Rome. L&#39;avocat juif, Tertulle, flatte malhonn&ecirc;tement le gouverneur romain et accuse ensuite Paul de trois crimes: exciter des divisions, &ecirc;tre un chef de file d&rsquo;une secte et profaner le temple juif de J&eacute;rusalem. Paul a affirm&eacute; quatre points: J&#39;adore le Dieu de nos p&egrave;res, je crois tout ce qui est en accord avec la Loi, j&#39;ai la m&ecirc;me esp&eacute;rance en Dieu que ces hommes, et je m&#39;efforce autant qu&#39;eux de garder ma conscience sans reproche. Paul a profit&eacute; de l&#39;occasion pour enseigner au gouverneur la foi en J&eacute;sus, la justice, la ma&icirc;trise de soi et le jugement. Il nous a montr&eacute; comment &ecirc;tre un t&eacute;moin fid&egrave;le, audacieux, mais tr&egrave;s respectueux en toute circonstance.</p>

<p>&nbsp;</p>
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

			<td class="social" @click="share('lesson', 'Paul présente sa défense devant le gouverneur romain Félix: ', '/content/M2/fra/multiply3/multiply348.html')">
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