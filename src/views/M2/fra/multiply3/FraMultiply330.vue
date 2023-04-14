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
                        <div class="chapter_number ltr"><h1>30.</h1></div>
                        <div class="chapter_title ltr"><h1>Les leaders discernent la volonté de Dieu d'aller vers les païens</h1></div>
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
	<li>Lisez ou observez Actes 15:1-35 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Actes 15:1-35</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Quelques hommes, venus de la Jud&eacute;e, enseignaient les fr&egrave;res, en disant: Si vous n&#39;&ecirc;tes circoncis selon le rite de Mo&iuml;se, vous ne pouvez &ecirc;tre sauv&eacute;s.</p>

<p><sup class="versenum">2&nbsp;</sup>Paul et Barnabas eurent avec eux un d&eacute;bat et une vive discussion; et les fr&egrave;res d&eacute;cid&egrave;rent que Paul et Barnabas, et quelques-uns des leurs, monteraient &agrave; J&eacute;rusalem vers les ap&ocirc;tres et les anciens, pour traiter cette question.</p>

<p><sup class="versenum">3&nbsp;</sup>Apr&egrave;s avoir &eacute;t&eacute; accompagn&eacute;s par l&#39;&Eacute;glise, ils poursuivirent leur route &agrave; travers la Ph&eacute;nicie et la Samarie, racontant la conversion des pa&iuml;ens, et ils caus&egrave;rent une grande joie &agrave; tous les fr&egrave;res.</p>

<p><sup class="versenum">4&nbsp;</sup>Arriv&eacute;s &agrave; J&eacute;rusalem, ils furent re&ccedil;us par l&#39;&Eacute;glise, les ap&ocirc;tres et les anciens, et ils racont&egrave;rent tout ce que Dieu avait fait avec eux.</p>

<p><sup class="versenum">5&nbsp;</sup>Alors quelques-uns du parti des pharisiens, qui avaient cru, se lev&egrave;rent, en disant qu&#39;il fallait circoncire les pa&iuml;ens et exiger l&#39;observation de la loi de Mo&iuml;se.</p>

<p><sup class="versenum">6&nbsp;</sup>Les ap&ocirc;tres et les anciens se r&eacute;unirent pour examiner cette affaire.</p>

<p><sup class="versenum">7&nbsp;</sup>Une grande discussion s&#39;&eacute;tant engag&eacute;e, Pierre se leva, et leur dit: Hommes fr&egrave;res, vous savez que d&egrave;s longtemps Dieu a fait un choix parmi vous, afin que, par ma bouche, les pa&iuml;ens entendissent la parole de l&#39;&Eacute;vangile et qu&#39;ils crussent.</p>

<p><sup class="versenum">8&nbsp;</sup>Et Dieu, qui conna&icirc;t les coeurs, leur a rendu t&eacute;moignage, en leur donnant le Saint Esprit comme &agrave; nous;</p>

<p><sup class="versenum">9&nbsp;</sup>il n&#39;a fait aucune diff&eacute;rence entre nous et eux, ayant purifi&eacute; leurs coeurs par la foi.</p>

<p><sup class="versenum">10&nbsp;</sup>Maintenant donc, pourquoi tentez-vous Dieu, en mettant sur le cou des disciples un joug que ni nos p&egrave;res ni nous n&#39;avons pu porter?</p>

<p><sup class="versenum">11&nbsp;</sup>Mais c&#39;est par la gr&acirc;ce du Seigneur J&eacute;sus que nous croyons &ecirc;tre sauv&eacute;s, de la m&ecirc;me mani&egrave;re qu&#39;eux.</p>

<p><sup class="versenum">12&nbsp;</sup>Toute l&#39;assembl&eacute;e garda le silence, et l&#39;on &eacute;couta Barnabas et Paul, qui racont&egrave;rent tous les miracles et les prodiges que Dieu avait faits par eux au milieu des pa&iuml;ens.</p>

<p><sup class="versenum">13&nbsp;</sup>Lorsqu&#39;ils eurent cess&eacute; de parler, Jacques prit la parole, et dit: Hommes fr&egrave;res, &eacute;coutez-moi!</p>

<p><sup class="versenum">14&nbsp;</sup>Simon a racont&eacute; comment Dieu a d&#39;abord jet&eacute; les regards sur les nations pour choisir du milieu d&#39;elles un peuple qui port&acirc;t son nom.</p>

<p><sup class="versenum">15&nbsp;</sup>Et avec cela s&#39;accordent les paroles des proph&egrave;tes, selon qu&#39;il est &eacute;crit:</p>

<p><sup class="versenum">16&nbsp;</sup>Apr&egrave;s cela, je reviendrai, et je rel&egrave;verai de sa chute la tente de David, J&#39;en r&eacute;parerai les ruines, et je la redresserai,</p>

<p><sup class="versenum">17&nbsp;</sup>Afin que le reste des hommes cherche le Seigneur, Ainsi que toutes les nations sur lesquelles mon nom est invoqu&eacute;, Dit le Seigneur, qui fait ces choses,</p>

<p><sup class="versenum">18&nbsp;</sup>Et &agrave; qui elles sont connues de toute &eacute;ternit&eacute;.</p>

<p><sup class="versenum">19&nbsp;</sup>C&#39;est pourquoi je suis d&#39;avis qu&#39;on ne cr&eacute;e pas des difficult&eacute;s &agrave; ceux des pa&iuml;ens qui se convertissent &agrave; Dieu,</p>

<p><sup class="versenum">20&nbsp;</sup>mais qu&#39;on leur &eacute;crive de s&#39;abstenir des souillures des idoles, de l&#39;impudicit&eacute;, des animaux &eacute;touff&eacute;s et du sang.</p>

<p><sup class="versenum">21&nbsp;</sup>Car, depuis bien des g&eacute;n&eacute;rations, Mo&iuml;se a dans chaque ville des gens qui le pr&ecirc;chent, puisqu&#39;on le lit tous les jours de sabbat dans les synagogues.</p>

<p><sup class="versenum">22&nbsp;</sup>Alors il parut bon aux ap&ocirc;tres et aux anciens, et &agrave; toute l&#39;&Eacute;glise, de choisir parmi eux et d&#39;envoyer &agrave; Antioche, avec Paul et Barsabas, Jude appel&eacute; Barnabas et Silas, hommes consid&eacute;r&eacute;s entre les fr&egrave;res.</p>

<p><sup class="versenum">23&nbsp;</sup>Ils les charg&egrave;rent d&#39;une lettre ainsi con&ccedil;ue: Les ap&ocirc;tres, les anciens, et les fr&egrave;res, aux fr&egrave;res d&#39;entre les pa&iuml;ens, qui sont &agrave; Antioche, en Syrie, et en Cilicie, salut!</p>

<p><sup class="versenum">24&nbsp;</sup>Ayant appris que quelques hommes partis de chez nous, et auxquels nous n&#39;avions donn&eacute; aucun ordre, vous ont troubl&eacute;s par leurs discours et ont &eacute;branl&eacute; vos &acirc;mes,</p>

<p><sup class="versenum">25&nbsp;</sup>nous avons jug&eacute; &agrave; propos, apr&egrave;s nous &ecirc;tre r&eacute;unis tous ensemble, de choisir des d&eacute;l&eacute;gu&eacute;s et de vous les envoyer avec nos bien-aim&eacute;s Barnabas et Paul,</p>

<p><sup class="versenum">26&nbsp;</sup>ces hommes qui ont expos&eacute; leur vie pour le nom de notre Seigneur J&eacute;sus Christ.</p>

<p><sup class="versenum">27&nbsp;</sup>Nous avons donc envoy&eacute; Jude et Silas, qui vous annonceront de leur bouche les m&ecirc;mes choses.</p>

<p><sup class="versenum">28&nbsp;</sup>Car il a paru bon au Saint Esprit et &agrave; nous de ne vous imposer d&#39;autre charge que ce qui est n&eacute;cessaire,</p>

<p><sup class="versenum">29&nbsp;</sup>savoir, de vous abstenir des viandes sacrifi&eacute;es aux idoles, du sang, des animaux &eacute;touff&eacute;s, et de l&#39;impudicit&eacute;, choses contre lesquelles vous vous trouverez bien de vous tenir en garde. Adieu.</p>

<p><sup class="versenum">30&nbsp;</sup>Eux donc, ayant pris cong&eacute; de l&#39;&Eacute;glise, all&egrave;rent &agrave; Antioche, o&ugrave; ils remirent la lettre &agrave; la multitude assembl&eacute;e.</p>

<p><sup class="versenum">31&nbsp;</sup>Apr&egrave;s l&#39;avoir lue, les fr&egrave;res furent r&eacute;jouis de l&#39;encouragement qu&#39;elle leur apportait.</p>

<p><sup class="versenum">32&nbsp;</sup>Jude et Silas, qui &eacute;taient eux-m&ecirc;mes proph&egrave;tes, les exhort&egrave;rent et les fortifi&egrave;rent par plusieurs discours.</p>

<p><sup class="versenum">33&nbsp;</sup>Au bout de quelque temps, les fr&egrave;res les laiss&egrave;rent en paix retourner vers ceux qui les avaient envoy&eacute;s.</p>

<p><sup class="versenum">34&nbsp;</sup>Toutefois Silas trouva bon de rester.</p>

<p><sup class="versenum">35&nbsp;</sup>Paul et Barnabas demeur&egrave;rent &agrave; Antioche, enseignant et annon&ccedil;ant, avec plusieurs autres, la bonne nouvelle de la parole du Seigneur.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply3/330.mp4" type="button" class="external-movie">
         Regardez Actes 15:1-35 </button>
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
	<li class="nobreak-final-final">Certains croyants juifs ont insist&eacute; sur le fait que sans la circoncision, les nouveaux convertis ne pourraient pas &ecirc;tre sauv&eacute;s. La circoncision &eacute;tait le signe donn&eacute; par Dieu que les Juifs &eacute;taient membres de l&#39;alliance de l&#39;Ancien Testament. Bien qu&rsquo;ils aient compris que le don de salut de Dieu &eacute;tait pour tous les peuples (<span class="popup-link" @click = "popUp('pop3')"> Actes 11:18</span>)&nbsp;&nbsp;

	<div class="popup invisible" id="pop3"><!-- begin bible -->
	<p><sup class="versenum">18&nbsp;</sup>Apr&egrave;s avoir entendu cela, ils se calm&egrave;rent, et ils glorifi&egrave;rent Dieu, en disant: Dieu a donc accord&eacute; la repentance aussi aux pa&iuml;ens, afin qu&#39;ils aient la vie.</p>
	<!-- end bible --></div>
	ils croyaient toujours que Dieu exigeait la circoncision et l&#39;observance de la Loi pour &ecirc;tre pleinement accept&eacute; dans le corps de Christ. La pratique du minist&egrave;re de Paul qui consiste &agrave; accepter les pa&iuml;ens comme membres du corps du Christ par la confession de foi et le bapt&ecirc;me seuls, &eacute;tait remise en cause.<br />
	<br />
	Mais nous voyons comment Paul &eacute;tait pr&ecirc;t &agrave; se soumettre &agrave; la d&eacute;cision du corps des croyants. L&#39;avenir de la mission de faire de toutes les nations des disciples &eacute;tait en jeu! Les leaders ont utilis&eacute; la pri&egrave;re, l&rsquo;&eacute;coute et le raisonnement attentifs, la r&eacute;flexion sur la Parole et l&rsquo;observation de la mani&egrave;re dont Dieu travaillait afin de discerner la volont&eacute; de Dieu. Ils ont clarifi&eacute; la doctrine qui a mis fin &agrave; la controverse et a promu la paix. J&eacute;sus avait ouvert la voie &agrave; tous les peuples pour qu&#39;ils reviennent vers le P&egrave;re.</li>
</ul>
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

			<td class="social" @click="share('lesson', 'Les leaders discernent la volonté de Dieu d\'aller vers les païens: ', '/content/M2/fra/multiply3/multiply330.html')">
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