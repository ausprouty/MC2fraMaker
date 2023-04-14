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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-multiply1-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>7.</h1></div>
                        <div class="chapter_title ltr"><h1>Demeurer en Jésus</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="back">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle">Regarder Derri&egrave;re</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Louange</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>Lisez un passage biblique et ex&eacute;cutez un chant d&rsquo;adoration.</p>

<ul>
	<li>Exemple: Lisez<span class="popup-link" @click = "popUp('pop1')">  Psaumes 16:7-11</span>

	<div class="popup invisible" id="pop1"><!-- begin bible -->
	<p><sup class="versenum">7&nbsp;</sup>Je b&eacute;nis l&#39;&Eacute;ternel, mon conseiller; La nuit m&ecirc;me mon coeur m&#39;exhorte.</p>

	<p><sup class="versenum">8&nbsp;</sup>J&#39;ai constamment l&#39;&Eacute;ternel sous mes yeux; Quand il est &agrave; ma droite, je ne chancelle pas.</p>

	<p><sup class="versenum">9&nbsp;</sup>Aussi mon coeur est dans la joie, mon esprit dans l&#39;all&eacute;gresse, Et mon corps repose en s&eacute;curit&eacute;.</p>

	<p><sup class="versenum">10&nbsp;</sup>Car tu ne livreras pas mon &acirc;me au s&eacute;jour des morts, Tu ne permettras pas que ton bien-aim&eacute; voie la corruption.</p>

	<p><sup class="versenum">11&nbsp;</sup>Tu me feras conna&icirc;tre le sentier de la vie; Il y a d&#39;abondantes joies devant ta face, Des d&eacute;lices &eacute;ternelles &agrave; ta droite.</p>
	<!-- end bible --></div>
	et apprenez une nouvelle chanson</li>
</ul>

</div>

<ul>
</ul>

<h2>Soin</h2>

<p>Prenez soin les uns des autres dans la pri&egrave;re, la relation d&rsquo;aide et l&rsquo;encouragement.</p>

<ul>
	<li>Demandez &agrave; chaque personne de raconter un moment fort et d&rsquo;expliquer un d&eacute;fi qu&rsquo;elle a eu cette semaine.</li>
	<li>Demandez, &laquo; Que voulez-vous que J&eacute;sus fasse pour vous cette semaine? &raquo; Priez pour vos besoins mutuels.</li>
</ul>

<h2>C&eacute;l&eacute;brer la Fid&eacute;lit&eacute;</h2>

<p>Encouragez l&rsquo;ob&eacute;issance &agrave; J&eacute;sus &agrave; travers une responsabilit&eacute; empreinte d&rsquo;amour</p>

<ul>
	<li>Demandez, &laquo; Que s&rsquo;est-il pass&eacute; pendant que vous avez fait confiance &agrave; Dieu pour vos objectifs et vos promesses je le ferai? &raquo;</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Projection de Vision</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>Projetez une vision de qui ils peuvent devenir en Christ ou de ce que Dieu peut faire &agrave; travers eux.</p>

<ul>
	<li class="nobreak-final-final">Exemple:<span class="popup-link" @click = "popUp('pop2')">  Jean 16</span>

	<div class="popup invisible" id="pop2"><!-- begin bible -->
	<div>
	<div>
	<div>
	<div>
	<div>
	<div>
	<p><sup class="versenum">1 </sup>Je vous ai dit ces choses, afin qu&#39;elles ne soient pas pour vous une occasion de chute.</p>

	<p><sup class="versenum">2&nbsp;</sup>Ils vous excluront des synagogues; et m&ecirc;me l&#39;heure vient o&ugrave; quiconque vous fera mourir croira rendre un culte &agrave; Dieu.</p>

	<p><sup class="versenum">3&nbsp;</sup>Et ils agiront ainsi, parce qu&#39;ils n&#39;ont connu ni le P&egrave;re ni moi.</p>

	<p><sup class="versenum">4&nbsp;</sup>Je vous ai dit ces choses, afin que, lorsque l&#39;heure sera venue, vous vous souveniez que je vous les ai dites. Je ne vous en ai pas parl&eacute; d&egrave;s le commencement, parce que j&#39;&eacute;tais avec vous.</p>

	<p><sup class="versenum">5&nbsp;</sup>Maintenant je m&#39;en vais vers celui qui m&#39;a envoy&eacute;, et aucun de vous ne me demande: O&ugrave; vas-tu?</p>

	<p><sup class="versenum">6&nbsp;</sup>Mais, parce que je vous ai dit ces choses, la tristesse a rempli votre coeur.</p>

	<p><sup class="versenum">7&nbsp;</sup>Cependant je vous dis la v&eacute;rit&eacute;: il vous est avantageux que je m&#39;en aille, car si je ne m&#39;en vais pas, le consolateur ne viendra pas vers vous; mais, si je m&#39;en vais, je vous l&#39;enverrai.</p>

	<p><sup class="versenum">8&nbsp;</sup>Et quand il sera venu, il convaincra le monde en ce qui concerne le p&eacute;ch&eacute;, la justice, et le jugement:</p>

	<p><sup class="versenum">9&nbsp;</sup>en ce qui concerne le p&eacute;ch&eacute;, parce qu&#39;ils ne croient pas en moi;</p>

	<p><sup class="versenum">10&nbsp;</sup>la justice, parce que je vais au P&egrave;re, et que vous ne me verrez plus;</p>

	<p><sup class="versenum">11&nbsp;</sup>le jugement, parce que le prince de ce monde est jug&eacute;.</p>

	<p><sup class="versenum">12&nbsp;</sup>J&#39;ai encore beaucoup de choses &agrave; vous dire, mais vous ne pouvez pas les porter maintenant.</p>

	<p><sup class="versenum">13&nbsp;</sup>Quand le consolateur sera venu, l&#39;Esprit de v&eacute;rit&eacute;, il vous conduira dans toute la v&eacute;rit&eacute;; car il ne parlera pas de lui-m&ecirc;me, mais il dira tout ce qu&#39;il aura entendu, et il vous annoncera les choses &agrave; venir.</p>

	<p><sup class="versenum">14&nbsp;</sup>Il me glorifiera, parce qu&#39;il prendra de ce qui est &agrave; moi, et vous l&#39;annoncera.</p>

	<p><sup class="versenum">15&nbsp;</sup>Tout ce que le P&egrave;re a est &agrave; moi; c&#39;est pourquoi j&#39;ai dit qu&#39;il prend de ce qui est &agrave; moi, et qu&#39;il vous l&#39;annoncera.</p>

	<p><sup class="versenum">16&nbsp;</sup>Encore un peu de temps, et vous ne me verrez plus; et puis encore un peu de temps, et vous me verrez, parce que je vais au P&egrave;re.</p>

	<p><sup class="versenum">17&nbsp;</sup>L&agrave;-dessus, quelques-uns de ses disciples dirent entre eux: Que signifie ce qu&#39;il nous dit: Encore un peu de temps, et vous ne me verrez plus; et puis encore un peu de temps, et vous me verrez? et: Parce que je vais au P&egrave;re?</p>

	<p><sup class="versenum">18&nbsp;</sup>Ils disaient donc: Que signifie ce qu&#39;il dit: Encore un peu de temps? Nous ne savons de quoi il parle.</p>

	<p><sup class="versenum">19&nbsp;</sup>J&eacute;sus, connut qu&#39;ils voulaient l&#39;interroger, leur dit: Vous vous questionnez les uns les autres sur ce que j&#39;ai dit: Encore un peu de temps, et vous ne me verrez plus; et puis encore un peu de temps, et vous me verrez.</p>

	<p><sup class="versenum">20&nbsp;</sup>En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, vous pleurerez et vous vous lamenterez, et le monde se r&eacute;jouira: vous serez dans la tristesse, mais votre tristesse se changera en joie.</p>

	<p><sup class="versenum">21&nbsp;</sup>La femme, lorsqu&#39;elle enfante, &eacute;prouve de la tristesse, parce que son heure est venue; mais, lorsqu&#39;elle a donn&eacute; le jour &agrave; l&#39;enfant, elle ne se souvient plus de la souffrance, &agrave; cause de la joie qu&#39;elle a de ce qu&#39;un homme est n&eacute; dans le monde.</p>

	<p><sup class="versenum">22&nbsp;</sup>Vous donc aussi, vous &ecirc;tes maintenant dans la tristesse; mais je vous reverrai, et votre coeur se r&eacute;jouira, et nul ne vous ravira votre joie.</p>

	<p><sup class="versenum">23&nbsp;</sup>En ce jour-l&agrave;, vous ne m&#39;interrogerez plus sur rien. En v&eacute;rit&eacute;, en v&eacute;rit&eacute;, je vous le dis, ce que vous demanderez au P&egrave;re, il vous le donnera en mon nom.</p>

	<p><sup class="versenum">24&nbsp;</sup>Jusqu&#39;&agrave; pr&eacute;sent vous n&#39;avez rien demand&eacute; en mon nom. Demandez, et vous recevrez, afin que votre joie soit parfaite.</p>

	<p><sup class="versenum">25&nbsp;</sup>Je vous ai dit ces choses en paraboles. L&#39;heure vient o&ugrave; je ne vous parlerai plus en paraboles, mais o&ugrave; je vous parlerai ouvertement du P&egrave;re.</p>

	<p><sup class="versenum">26&nbsp;</sup>En ce jour, vous demanderez en mon nom, et je ne vous dis pas que je prierai le P&egrave;re pour vous;</p>

	<p><sup class="versenum">27&nbsp;</sup>car le P&egrave;re lui-m&ecirc;me vous aime, parce que vous m&#39;avez aim&eacute;, et que vous avez cru que je suis sorti de Dieu.</p>

	<p><sup class="versenum">28&nbsp;</sup>Je suis sorti du P&egrave;re, et je suis venu dans le monde; maintenant je quitte le monde, et je vais au P&egrave;re.</p>

	<p><sup class="versenum">29&nbsp;</sup>Ses disciples lui dirent: Voici, maintenant tu parles ouvertement, et tu n&#39;emploies aucune parabole.</p>

	<p><sup class="versenum">30&nbsp;</sup>Maintenant nous savons que tu sais toutes choses, et que tu n&#39;as pas besoin que personne t&#39;interroge; c&#39;est pourquoi nous croyons que tu es sorti de Dieu.</p>

	<p><sup class="versenum">31&nbsp;</sup>J&eacute;sus leur r&eacute;pondit: Vous croyez maintenant.</p>

	<p><sup class="versenum">32&nbsp;</sup>Voici, l&#39;heure vient, et elle est d&eacute;j&agrave; venue, o&ugrave; vous serez dispers&eacute;s chacun de son c&ocirc;t&eacute;, et o&ugrave; vous me laisserez seul; mais je ne suis pas seul, car le P&egrave;re est avec moi.</p>

	<p><sup class="versenum">33&nbsp;</sup>Je vous ai dit ces choses, afin que vous ayez la paix en moi. Vous aurez des tribulations dans le monde; mais prenez courage, j&#39;ai vaincu le monde.</p>
	</div>
	</div>
	</div>
	</div>
	</div>
	</div>
	<!-- end bible --></div>
	nous enseigne que le Saint Espit agit dans le coeur de ceux qui sont autour de nous . Il les convainc de leur p&eacute;ch&eacute;. Il cr&eacute;e en eux le d&eacute;sir d&rsquo;&ecirc;tre juste envers Dieu. Il cr&eacute;e en eux le d&eacute;sir d&rsquo;&eacute;viter la peur de la mort, le jugement &eacute;ternel. Il d&eacute;truit en eux les objections de leur pens&eacute;e et de leur c&oelig;ur. Notre r&ocirc;le est d&rsquo;amener ces personnes au Seigneur &agrave; travers le t&eacute;moignage, chercher ceux dont les c&oelig;urs sont dispos&eacute;s. Encourageons-nous mutuellement en nous rappelant que l&rsquo;Esprit est d&eacute;j&agrave; &agrave; l&rsquo;&oelig;uvre avant m&ecirc;me que nous allions t&eacute;moigner.</li>
</ul>

</div>
</div>

<div class="up">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle">Regarder en Haut</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary2" class="summary"><h2>+ Contexte</h2></div>
<div class="collapsed" id ="Text2">
<!-- end default revealSummary -->

<p>La nuit avant que J&eacute;sus ne fut crucifi&eacute;, il a din&eacute; avec ses 12 disciples. Il leur a dit qu&rsquo;il allait leur envoyer le Consolateur, l&rsquo;Esprit Saint, qui sera avec eux pour toujours. Il leur enseigna qu&rsquo;&agrave; travers la pr&eacute;sence du Saint Esprit vivant en eux, Lui-aussi sera avec eux. Cette histoire utilise l&rsquo;image d&rsquo;une vigne et de ses branches pour d&eacute;crire ce &agrave; quoi notre relation avec le p&egrave;re devrait ressembler.</p>

</div>

<h2>Lire</h2>

<ul>
	<li>Lisez ou observez Jean 15:1-11 deux fois pendant que les autres &eacute;coutent.</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Lire Jean 15:1-11</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<p><sup class="versenum">1 </sup>Je suis le vrai cep, et mon P&egrave;re est le vigneron.</p>

<p><sup class="versenum">2&nbsp;</sup>Tout sarment qui est en moi et qui ne porte pas de fruit, il le retranche; et tout sarment qui porte du fruit, il l&#39;&eacute;monde, afin qu&#39;il porte encore plus de fruit.</p>

<p><sup class="versenum">3&nbsp;</sup>D&eacute;j&agrave; vous &ecirc;tes purs, &agrave; cause de la parole que je vous ai annonc&eacute;e.</p>

<p><sup class="versenum">4&nbsp;</sup>Demeurez en moi, et je demeurerai en vous. Comme le sarment ne peut de lui-m&ecirc;me porter du fruit, s&#39;il ne demeure attach&eacute; au cep, ainsi vous ne le pouvez non plus, si vous ne demeurez en moi.</p>

<p><sup class="versenum">5&nbsp;</sup>Je suis le cep, vous &ecirc;tes les sarments. Celui qui demeure en moi et en qui je demeure porte beaucoup de fruit, car sans moi vous ne pouvez rien faire.</p>

<p><sup class="versenum">6&nbsp;</sup>Si quelqu&#39;un ne demeure pas en moi, il est jet&eacute; dehors, comme le sarment, et il s&egrave;che; puis on ramasse les sarments, on les jette au feu, et ils br&ucirc;lent.</p>

<p><sup class="versenum">7&nbsp;</sup>Si vous demeurez en moi, et que mes paroles demeurent en vous, demandez ce que vous voudrez, et cela vous sera accord&eacute;.</p>

<p><sup class="versenum">8&nbsp;</sup>Si vous portez beaucoup de fruit, c&#39;est ainsi que mon P&egrave;re sera glorifi&eacute;, et que vous serez mes disciples.</p>

<p><sup class="versenum">9&nbsp;</sup>Comme le P&egrave;re m&#39;a aim&eacute;, je vous ai aussi aim&eacute;s. Demeurez dans mon amour.</p>

<p><sup class="versenum">10&nbsp;</sup>Si vous gardez mes commandements, vous demeurerez dans mon amour, de m&ecirc;me que j&#39;ai gard&eacute; les commandements de mon P&egrave;re, et que je demeure dans son amour.</p>

<p><sup class="versenum">11&nbsp;</sup>Je vous ai dit ces choses, afin que ma joie soit en vous, et que votre joie soit parfaite.</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/fra/video/multiply1/107.mp4" type="button" class="external-movie">
         Regardez &nbsp;Jean 15:1-11&nbsp; </button>
    <div class="collapsed"></div>

<h2>Discussion de D&eacute;couverte</h2>

<ul>
	<li>Chacun dit ce qui a retenu son attention (ou ce qu&rsquo;il a aim&eacute; le plus) et pourquoi.</li>
	<li>Pourquoi pensez-vous que cette histoire est importante?</li>
	<li>Comment pouvons-nous vivre diff&eacute;remment maintenant que nous connaissons cette histoire (passage)?</li>
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

<ul>
	<li>Relisez l&rsquo;histoire. D&eacute;signez quelqu&rsquo;un pour raconter l&rsquo;histoire et demandez au groupe de corriger si n&eacute;cessaire.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary3" class="summary"><h2>+ R&eacute;sum&eacute;</h2></div>
<div class="collapsed" id ="Text3">
<!-- end default revealSummary -->

<p>Sans J&eacute;sus, nous ne pouvons rien faire. Nous ne pourrons avoir une vie fructueuse que si nous d&eacute;pendons de Lui et vivons en Lui. Cela sera possible si nous nous soumettons en toute ob&eacute;issance &agrave; Ses voies, ce qui permettra &agrave; sa vie de d&eacute;border en nous. Ainsi, nous pouvons porter des fruits pour la gloire de Dieu. En d&rsquo;autres termes, nous devons laisser l&rsquo;Esprit de Christ, l&rsquo;Esprit Saint diriger et renforcer nos vies par la foi.</p>

</div>

<p><span class="for-enrichment">Pour une &eacute;tude plus approfondi: Lisez le message Transmissible #4: Comment marcher par l&rsquo;Esprit et discutez avec un autre membre du groupe</span>.</p>
</div>

<div class="forward">
<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle">Regarder Devant</div>
</div>

<!-- begin default revealSummary -->
<div id="Summary4" class="summary"><h2>+ Se Pr&eacute;parer pour la Mission</h2></div>
<div class="collapsed" id ="Text4">
<!-- end default revealSummary -->

<ul>
	<li>R&eacute;visez les principes de la Respiration Spirituelle de la le&ccedil;on 3, &laquo; Rester en Phase avec l&rsquo;Esprit Saint &raquo;.</li>
	<li>Pratiquez n&#39;importe quelle comp&eacute;tence ou sujet des le&ccedil;ons pr&eacute;c&eacute;dentes si n&eacute;cessaire</li>
</ul>

</div>

<ul>
</ul>

<h2>Aller en Mission&nbsp;</h2>

<ul>
	<li>Identifiez 5 personnes de votre liste de r&eacute;seau, &agrave; qui vous raconterez l&rsquo;histoire ou annoncerez la bonne nouvelle cette semaine</li>
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

<ul>
	<li>Confiez les objectifs de chacun au Seigneur. Demandez au Seigneur de nous aider tous &agrave; &ecirc;tre fid&egrave;les et de nous utiliser pour initier un mouvement de faiseurs de disciples.</li>
</ul>
</div>

<div class="for-enrichment">Pour en savoir davantage veuillez lire le <!-- begin linkInternal capacitor-->
<span id= "Return1" class="internal-link" @click="this.goToPageAndSetReturn('/M2/fra/tc/ct04', '#1')">
    Message transmissible N&deg; 4 : Comment marcher par l&#39;Esprit 
</span>
<!-- end linkInternal capacitor-->
 et en discuter avec un autre membre du groupe.</div>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Demeurer en Jésus: ', '/content/M2/fra/multiply1/multiply107.html')">
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