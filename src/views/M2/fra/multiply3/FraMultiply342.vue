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
                        <div class="chapter_number ltr"><h1>42.</h1></div>
                        <div class="chapter_title ltr"><h1>Dernière instruction à l'endroit des anciens d'Éphèse</h1></div>
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
	<li>Lisez ou observez Actes 20:13-38 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 20:13-38</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">13&nbsp;</sup>Pour nous, nous pr&eacute;c&eacute;d&acirc;mes Paul sur le navire, et nous f&icirc;mes voile pour Assos, o&ugrave; nous avions convenu de le reprendre, parce qu&#39;il devait faire la route &agrave; pied.</p>

<p><sup class="versenum">14&nbsp;</sup>Lorsqu&#39;il nous eut rejoints &agrave; Assos, nous le pr&icirc;mes &agrave; bord, et nous all&acirc;mes &agrave; Mytil&egrave;ne.</p>

<p><sup class="versenum">15&nbsp;</sup>De l&agrave;, continuant par mer, nous arriv&acirc;mes le lendemain vis-&agrave;-vis de Chios. Le jour suivant, nous cingl&acirc;mes vers Samos, et le jour d&#39;apr&egrave;s nous v&icirc;nmes &agrave; Milet.</p>

<p><sup class="versenum">16&nbsp;</sup>Paul avait r&eacute;solu de passer devant &Eacute;ph&egrave;se sans s&#39;y arr&ecirc;ter, afin de ne pas perdre de temps en Asie; car il se h&acirc;tait pour se trouver, si cela lui &eacute;tait possible, &agrave; J&eacute;rusalem le jour de la Pentec&ocirc;te.</p>

<p><sup class="versenum">17&nbsp;</sup>Cependant, de Milet Paul envoya chercher &agrave; &Eacute;ph&egrave;se les anciens de l&#39;&Eacute;glise.</p>

<p><sup class="versenum">18&nbsp;</sup>Lorsqu&#39;ils furent arriv&eacute;s vers lui, il leur dit: Vous savez de quelle mani&egrave;re, depuis le premier jour o&ugrave; je suis entr&eacute; en Asie, je me suis sans cesse conduit avec vous,</p>

<p><sup class="versenum">19&nbsp;</sup>servant le Seigneur en toute humilit&eacute;, avec larmes, et au milieu des &eacute;preuves que me suscitaient les emb&ucirc;ches des Juifs.</p>

<p><sup class="versenum">20&nbsp;</sup>Vous savez que je n&#39;ai rien cach&eacute; de ce qui vous &eacute;tait utile, et que je n&#39;ai pas craint de vous pr&ecirc;cher et de vous enseigner publiquement et dans les maisons,</p>

<p><sup class="versenum">21&nbsp;</sup>annon&ccedil;ant aux Juifs et aux Grecs la repentance envers Dieu et la foi en notre Seigneur J&eacute;sus Christ.</p>

<p><sup class="versenum">22&nbsp;</sup>Et maintenant voici, li&eacute; par l&#39;Esprit, je vais &agrave; J&eacute;rusalem, ne sachant pas ce qui m&#39;y arrivera;</p>

<p><sup class="versenum">23&nbsp;</sup>seulement, de ville en ville, l&#39;Esprit Saint m&#39;avertit que des liens et des tribulations m&#39;attendent.</p>

<p><sup class="versenum">24&nbsp;</sup>Mais je ne fais pour moi-m&ecirc;me aucun cas de ma vie, comme si elle m&#39;&eacute;tait pr&eacute;cieuse, pourvu que j&#39;accomplisse ma course avec joie, et le minist&egrave;re que j&#39;ai re&ccedil;u du Seigneur J&eacute;sus, d&#39;annoncer la bonne nouvelle de la gr&acirc;ce de Dieu.</p>

<p><sup class="versenum">25&nbsp;</sup>Et maintenant voici, je sais que vous ne verrez plus mon visage, vous tous au milieu desquels j&#39;ai pass&eacute; en pr&ecirc;chant le royaume de Dieu.</p>

<p><sup class="versenum">26&nbsp;</sup>C&#39;est pourquoi je vous d&eacute;clare aujourd&#39;hui que je suis pur du sang de vous tous,</p>

<p><sup class="versenum">27&nbsp;</sup>car je vous ai annonc&eacute; tout le conseil de Dieu, sans en rien cacher.</p>

<p><sup class="versenum">28&nbsp;</sup>Prenez donc garde &agrave; vous-m&ecirc;mes, et &agrave; tout le troupeau sur lequel le Saint Esprit vous a &eacute;tablis &eacute;v&ecirc;ques, pour pa&icirc;tre l&#39;&Eacute;glise du Seigneur, qu&#39;il s&#39;est acquise par son propre sang.</p>

<p><sup class="versenum">29&nbsp;</sup>Je sais qu&#39;il s&#39;introduira parmi vous, apr&egrave;s mon d&eacute;part, des loups cruels qui n&#39;&eacute;pargneront pas le troupeau,</p>

<p><sup class="versenum">30&nbsp;</sup>et qu&#39;il s&#39;&eacute;l&egrave;vera du milieu de vous des hommes qui enseigneront des choses pernicieuses, pour entra&icirc;ner les disciples apr&egrave;s eux.</p>

<p><sup class="versenum">31&nbsp;</sup>Veillez donc, vous souvenant que, durant trois ann&eacute;es, je n&#39;ai cess&eacute; nuit et jour d&#39;exhorter avec larmes chacun de vous.</p>

<p><sup class="versenum">32&nbsp;</sup>Et maintenant je vous recommande &agrave; Dieu et &agrave; la parole de sa gr&acirc;ce, &agrave; celui qui peut &eacute;difier et donner l&#39;h&eacute;ritage avec tous les sanctifi&eacute;s.</p>

<p><sup class="versenum">33&nbsp;</sup>Je n&#39;ai d&eacute;sir&eacute; ni l&#39;argent, ni l&#39;or, ni les v&ecirc;tements de personne.</p>

<p><sup class="versenum">34&nbsp;</sup>Vous savez vous-m&ecirc;mes que ces mains ont pourvu &agrave; mes besoins et &agrave; ceux des personnes qui &eacute;taient avec moi.</p>

<p><sup class="versenum">35&nbsp;</sup>Je vous ai montr&eacute; de toutes mani&egrave;res que c&#39;est en travaillant ainsi qu&#39;il faut soutenir les faibles, et se rappeler les paroles du Seigneur, qui a dit lui-m&ecirc;me: Il y a plus de bonheur &agrave; donner qu&#39;&agrave; recevoir.</p>

<p><sup class="versenum">36&nbsp;</sup>Apr&egrave;s avoir ainsi parl&eacute;, il se mit &agrave; genoux, et il pria avec eux tous.</p>

<p><sup class="versenum">37&nbsp;</sup>Et tous fondirent en larmes, et, se jetant au cou de Paul,</p>

<p><sup class="versenum">38&nbsp;</sup>ils l&#39;embrassaient, afflig&eacute;s surtout de ce qu&#39;il avait dit qu&#39;ils ne verraient plus son visage. Et ils l&#39;accompagn&egrave;rent jusqu&#39;au navire.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/342.mp4" type="button" class="external-movie">
         Regardez &nbsp;Actes 20:13-38&nbsp; </button>
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

<ul>
	<li class="nobreak-final-final">Sur son chemin vers J&eacute;rusalem, Paul et l&rsquo;&eacute;quipe minist&eacute;rielle se sont arr&ecirc;t&eacute;s &agrave; Mytil&egrave;ne. Paul a appel&eacute; les anciens d&rsquo;&Eacute;ph&egrave;se &agrave; venir afin qu&rsquo;il &nbsp;puisse parler avec eux une derni&egrave;re fois. Des exp&eacute;riences de Paul, on apprend beaucoup sur la pers&eacute;v&eacute;rance qu&rsquo;il faut pour implanter des &eacute;glises dans les villes des non-chr&eacute;tiens. Paul a rencontr&eacute; plusieurs proc&egrave;s et &eacute;preuves, mais il a toujours dit la v&eacute;rit&eacute; aux &Eacute;ph&eacute;siens. Il n&rsquo;a jamais chang&eacute; son message pour plaire au gens. Paul a aussi &eacute;t&eacute; un mod&egrave;le d&rsquo;abandon total &agrave; la volont&eacute; du Seigneur, m&ecirc;me au milieu de la souffrance. On apprend beaucoup sur l&rsquo;importance du r&ocirc;le que les anciens ont. Ils doivent veiller sur leur vie et &ecirc;tre un mod&egrave;le dans la marche avec J&eacute;sus. Ils doivent aussi garder le peuple de Dieu et le nourrir avec l&rsquo;enseignant la Parole de J&eacute;sus. J&eacute;sus a enseign&eacute; que la nature du royaume de Dieu devrait toujours inclure la pr&eacute;sence du mal (<span class="popup-link" @click = "popUp('pop3')"> Matthieu 13 :24-30</span>).

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">24&nbsp;</sup>Il leur proposa une autre parabole, et il dit: Le royaume des cieux est semblable &agrave; un homme qui a sem&eacute; une bonne semence dans son champ.</p>

	<p><sup class="versenum">25&nbsp;</sup>Mais, pendant que les gens dormaient, son ennemi vint, sema de l&#39;ivraie parmi le bl&eacute;, et s&#39;en alla.</p>

	<p><sup class="versenum">26&nbsp;</sup>Lorsque l&#39;herbe eut pouss&eacute; et donn&eacute; du fruit, l&#39;ivraie parut aussi.</p>

	<p><sup class="versenum">27&nbsp;</sup>Les serviteurs du ma&icirc;tre de la maison vinrent lui dire: Seigneur, n&#39;as-tu pas sem&eacute; une bonne semence dans ton champ? D&#39;o&ugrave; vient donc qu&#39;il y a de l&#39;ivraie?</p>

	<p><sup class="versenum">28&nbsp;</sup>Il leur r&eacute;pondit: C&#39;est un ennemi qui a fait cela. Et les serviteurs lui dirent: Veux-tu que nous allions l&#39;arracher?</p>

	<p><sup class="versenum">29&nbsp;</sup>Non, dit-il, de peur qu&#39;en arrachant l&#39;ivraie, vous ne d&eacute;raciniez en m&ecirc;me temps le bl&eacute;.</p>

	<p><sup class="versenum">30&nbsp;</sup>Laissez cro&icirc;tre ensemble l&#39;un et l&#39;autre jusqu&#39;&agrave; la moisson, et, &agrave; l&#39;&eacute;poque de la moisson, je dirai aux moissonneurs: Arrachez d&#39;abord l&#39;ivraie, et liez-la en gerbes pour la br&ucirc;ler, mais amassez le bl&eacute; dans mon grenier.</p>
	<!-- end bible --></div>
	Paul savait qu&rsquo;ils feraient face aux dangers des faux enseignants dont le d&eacute;sir &eacute;tait de d&eacute;truire les croyants. Cette p&eacute;riode se termine par la d&eacute;claration de Paul qui dit que son &oelig;uvre &eacute;tait accomplie dans la partie Est de l&rsquo;Empire Romain. (<span class="popup-link" @click = "popUp('pop4')"> Romains 15:19</span>).&nbsp;

	<div class="popup invisible" id="pop4"><!-- begin bible -->
	<p><sup class="versenum">19&nbsp;</sup>par la puissance des miracles et des prodiges, par la puissance de l&#39;Esprit de Dieu, en sorte que, depuis J&eacute;rusalem et les pays voisins jusqu&#39;en Illyrie, j&#39;ai abondamment r&eacute;pandu l&#39;&Eacute;vangile de Christ.</p>
	</div>
	</li>
</ul>

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

			<td class="social" @click="share('lesson', 'Dernière instruction à l\'endroit des anciens d\'Éphèse: ', '/content/M2/fra/multiply3/multiply342.html')">
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