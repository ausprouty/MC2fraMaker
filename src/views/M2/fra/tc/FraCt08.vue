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
    <div class="nav full internal-link" @click="this.pageGoBack('fra-tc-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>8.</h1></div>
                        <div class="chapter_title ltr"><h1>Comment Aimer par la Foi</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <p>Peut-&ecirc;tre que vous avez connu quelqu&#39;un comme Georgia ... vous ne la classeriez pas comme une amie, mais elle n&#39;est pas non plus un ennemi. C&#39;est une personne que vous tol&eacute;rez parce qu&#39;elle partage un bureau dans la m&ecirc;me suite que vous. Elle dit qu&#39;elle va &agrave; l&#39;&eacute;glise, mais elle n&#39;agit pas comme un enfant de Dieu. Sa conversation est parsem&eacute;e de mots de neuf lettres et agr&eacute;ment&eacute;e des plus r&eacute;centes &laquo;nouvelles&raquo; sur ses coll&egrave;gues de service.<br />
<br />
Vous avez gard&eacute; vos distances parce que vous ne voulez pas &ecirc;tre associ&eacute;s &agrave; elle, mais&nbsp; Georgia a besoin d&#39;&ecirc;tre aim&eacute;e, et Dieu a dispos&eacute; votre c&oelig;ur &agrave; l&#39;aimer. Est-il vraiment possible d&#39;aimer quelqu&#39;un comme &ccedil;a?<br />
<br />
<em>Le plus grand besoin de l&rsquo;homme,</em><em> c&rsquo;est d&rsquo;&ecirc;tre aim&eacute;.</em> Nous cherchons tous &agrave; le donner, et nous aspirons tous &agrave; le recevoir. Peu de barri&egrave;res peuvent r&eacute;sister &agrave; la puissante force de l&#39;amour, en particulier l&#39;amour de Dieu. C&#39;est l&#39;amour de Dieu qui a chang&eacute; le cours de l&#39;histoire. L&#39;amour des chr&eacute;tiens du premier si&egrave;cle les uns pour les autres &eacute;tait ce qui les distinguait du reste du monde.<br />
<br />
Au temps du Christ, la haine &eacute;tait la pratique courante pour les Grecs, les Romains - et les Juifs. Le racisme, les syst&egrave;mes de classe sociale, les guerres et les pr&eacute;jug&eacute;s r&eacute;gnaient et faisaient la loi. Donc, lorsque les disciples de J&eacute;sus - un groupe fortement diversifi&eacute; - ont manifest&eacute; de l&#39;amour les uns envers les autres, le reste du monde s&#39;est r&eacute;veill&eacute; et s&rsquo;en est rendu compte. J&eacute;sus avait dit, &laquo;&nbsp;A ceci tous conna&icirc;tront que vous &ecirc;tes mes disciples, si vous avez de l&rsquo;amour les uns pour les autres&nbsp;&raquo; (Jean 13:35). Il avait raison. Les spectateurs ont regard&eacute; et ont r&eacute;pondu avec &eacute;tonnement, &laquo;&nbsp;Voyez comment ces gens s&#39;aiment!&nbsp;&raquo; Bient&ocirc;t beaucoup d&#39;entre eux ont rejoint la r&eacute;volution de l&#39;amour qui a balay&eacute; leur monde.<br />
<br />
La langue grecque nous donne une meilleure compr&eacute;hension des diverses significations, m&ecirc;me celles qui n&rsquo;ont pas de rapport, mais le grec est beaucoup plus sp&eacute;cifique.<br />
<br />
<em>Eros</em> est un mot qui signifie amour, mais il parle en r&eacute;alit&eacute; de d&eacute;sir sensuel; il n&#39;est pas utilis&eacute; dans le Nouveau Testament.<br />
<br />
<em>Phileo</em>, un deuxi&egrave;me mot pour l&#39;amour, se r&eacute;f&egrave;re au genre d&#39;amour trouv&eacute; entre amis ou parents, et donne le sentiment d&#39;aimer quelqu&#39;un parce qu&#39;il est digne de notre amour.<br />
<br />
<em>Agape</em> est le troisi&egrave;me, et le genre d&rsquo;amour le plus pur. Il est utilis&eacute; pour d&eacute;crire l&#39;amour que Dieu a pour nous. Il n&#39;est pas simplement exprim&eacute; par les &eacute;motions, mais c&#39;est souvent un acte de volont&eacute;. C&#39;est l&#39;amour surnaturel de Dieu pour nous, r&eacute;v&eacute;l&eacute; supr&ecirc;mement par la mort de notre Seigneur sur la croix &agrave; notre place. C&#39;est l&#39;amour divin qu&#39;il d&eacute;sire reproduire en nous et &agrave; travers nous pour les autres, et sa source est le Saint-Esprit.<br />
<br />
L&rsquo;amour <em>Agape</em> est bas&eacute; sur le caract&egrave;re de la personne qui manifeste l&#39;amour. Cela ne d&eacute;pend pas de savoir si le sujet de l&#39;amour en est digne. Parfois, c&#39;est l&#39;amour &laquo;&nbsp;malgr&eacute;&nbsp;&raquo;, mais n&#39;aime jamais &laquo;&nbsp;&agrave; cause de&nbsp;&raquo;</p>

<h2>Un Commandement Nouveau</h2>

<p>Le Seigneur J&eacute;sus a donn&eacute; &agrave; Ses disciples un commandement nouveau qui s&rsquo;applique &agrave; nous aujourd&rsquo;hui. Il dit&nbsp;: &laquo;&nbsp;Aimez-vous les uns les autres&nbsp;; comme je vous ai aim&eacute;s,&nbsp;&raquo; (Jean 13:34, LSG). Mais &agrave; quel genre d&rsquo;amour se r&eacute;f&eacute;rait-IL? Pour r&eacute;pondre &agrave; cela, nous devons explorer le genre d&rsquo;amour dont-Il nous a aim&eacute;s.<br />
<br />
L&#39;amour de Dieu a &eacute;t&eacute; exprim&eacute; &agrave; travers son Fils unique, J&eacute;sus, &laquo;&nbsp;afin que quiconque croit en lui ne p&eacute;risse point, mais qu&rsquo;il ait la vie &eacute;ternelle.&nbsp;&raquo; (Jean 3:16). C&#39;est le m&ecirc;me amour qui a gard&eacute; le Fils de Dieu suspendu &agrave; notre croix pour mourir pour nos p&eacute;ch&eacute;s. C&#39;est l&#39;amour divin, surnaturel, inconditionnel que Dieu met &agrave; la disposition des croyants, avec l&#39;ordre que nous devons nous aimer les uns les autres.<br />
<br />
Est-il possible que vous et moi puissions aimer d&rsquo;un&nbsp; amour divin? Si le jour de la Pentec&ocirc;te n&#39;avait pas eu lieu, l&#39;amour de Dieu n&#39;aurait jamais &eacute;t&eacute; reproduit sous forme humaine. Mais avec l&#39;effusion du Saint-Esprit, les disciples se sont trouv&eacute;s capables de s&#39;aimer comme J&eacute;sus l&#39;avait fait. Ils ont m&ecirc;me miraculeusement parvenus &agrave; aimer leurs ennemis, les foules en col&egrave;re qui avaient crucifi&eacute; leur Seigneur. Les personnes m&ecirc;mes qui ont menac&eacute; leur vie ont &eacute;t&eacute; vues sous un jour nouveau.<br />
<br />
Cet amour, cet amour agape, est &agrave; notre disposition aujourd&#39;hui. Ce n&#39;est pas une exp&eacute;rience &eacute;motionnelle, mais une puissance divine, surnaturelle, qui vient du P&egrave;re. Ce genre d&#39;amour coule &agrave; travers le Saint-Esprit &agrave; nous, et &agrave; travers nous &agrave; ceux dans le monde qui nous entoure. C&#39;est ce qui nous permet d&#39;aimer quelqu&#39;un comme Georgia.<br />
<br />
Au fur et &agrave; mesure que nous acqu&eacute;rons l&rsquo;amour de Dieu en nous et apprenons &agrave; int&eacute;grer Sa capacit&eacute; d&rsquo;amour dans nos vies, il y a plusieurs choses que nous devons savoir au sujet de cet amour puissant qu&rsquo;est le n&ocirc;tre.<br />
<br />
<em>Dieu nous aime d&rsquo;un AMOUR INCONDITIONEL! </em>Nous sommes aim&eacute;s &agrave; cause de Lui et non &agrave; cause de nous. Son amour pour nous n&rsquo;est jamais bas&eacute; sur notre performance. Il nous aime malgr&eacute; notre d&eacute;sob&eacute;issance, faiblesse, p&eacute;ch&eacute; et &eacute;go&iuml;sme. Son amour est si grand qu&rsquo;Il a choisi de nous aimer, et m&ecirc;me mourir&nbsp; pour nous lorsque que nous &eacute;tions encore des p&eacute;cheurs (Romains 5:8). Son amour est inconditionnel et compl&egrave;tement imm&eacute;rit&eacute;.<br />
<br />
<em>On nous recommande d&rsquo;aimer.</em> Un jeune avocat riche et prosp&egrave;re du Sanh&eacute;drin a autrefois abord&eacute; J&eacute;sus avec une question que son propre esprit &eacute;clair&eacute; et entra&icirc;n&eacute; ne pouvait pas r&eacute;pondre. &laquo;&nbsp;Ma&icirc;tre,&nbsp;&raquo; dit-il, &laquo;&nbsp;quel est le plus grand commandement de la loi&nbsp;&raquo;? J&eacute;sus r&eacute;pondit sans h&eacute;sitation. &laquo;&nbsp;Tu aimeras le Seigneur, ton Dieu, de tout ton c&oelig;ur, de toute ton &acirc;me, et de toute ta pens&eacute;e.&nbsp;&raquo; Il dit. &laquo;&nbsp;C&rsquo;est le premier et le plus grand commandement&nbsp;&raquo;. Et voici le second, qui lui est semblable&nbsp;: &laquo;&nbsp;Tu aimeras ton prochain comme toi-m&ecirc;me.&nbsp;&raquo; (Matthieu 22: 36-40).<br />
<br />
Tout autre commandement, toute autre loi donn&eacute; par Dieu ou instaur&eacute; par l&rsquo;homme, trouve sa racine dans l&rsquo;un de ces deux commandements dont J&eacute;sus dit &ecirc;tre le plus important de tout. Gardez ces deux lois et vous les accomplissez toutes. Et puis J&eacute;sus en ajoute&nbsp;: &laquo;&nbsp;Ce que je vous commande, c&rsquo;est de vous aimer les uns les autres.&nbsp;&raquo; (Jean 15:17).</p>

<h2>Nos propres efforts</h2>

<p><em>Nous ne pouvons pas aimer de notre propre force.</em> Nous refusons souvent d&#39;aimer les gens d&eacute;sagr&eacute;ables. Il est plus facile d&#39;aimer les &laquo;&nbsp;belles&nbsp;&raquo; personnes. Ou aimer ceux qui sont bons envers nous et ceux qui appr&eacute;cient ce que nous faisons pour eux. Pourquoi aimer quelqu&#39;un qui n&#39;est pas attrayant, ou particulier, ou grincheux ou d&eacute;sagr&eacute;able? Ou pourquoi m&ecirc;me essayer d&#39;aimer ceux qui ne nous aiment pas? D&#39;abord, parce que Dieu dit que nous devons. Deuxi&egrave;mement, il fournit la force d&#39;ob&eacute;ir &agrave; chaque commandement. En nous-m&ecirc;mes nous n&#39;avons ni le pouvoir ni la motivation d&#39;aimer les personnes peu aimables, et la Bible explique pourquoi: &laquo;&nbsp;car l&rsquo;affection de la chair est inimiti&eacute; contre Dieu, parce qu&rsquo;elle ne se soumet pas &agrave; la loi de Dieu, et qu&rsquo;elle ne le peut m&ecirc;me pas.&nbsp;&raquo; (Romains 8:7, LSG).<br />
<br />
Nous ne pouvons pas d&eacute;montrer l&#39;amour agape, l&#39;amour inconditionnel de Dieu pour les autres, par nos propres efforts. Nous pouvons r&eacute;soudre &agrave; plusieurs reprises d&#39;aimer quelqu&#39;un qui nous agace, et en quelques jours (si cela prend autant de temps) nous retombons dans nos anciens sch&eacute;mas d&#39;&eacute;vitement et de procrastination, ou ce en quoi nous sommes meilleurs. Par nature, nous sommes trop fiers de &laquo;nous abaisser dans une certaine mesure si humble&raquo; et d&#39;essayer d&#39;aimer quelqu&#39;un qui ne nous aime pas en retour ou m&ecirc;me d&#39;appr&eacute;cier nos efforts en son nom. Notre cruaut&eacute; et nos jalousies, notre fiert&eacute; et notre &eacute;go&iuml;sme bloquent notre chemin vers l&#39;ob&eacute;issance. Il est humainement impossible d&#39;aimer les autres comme J&eacute;sus nous dit d&#39;aimer.</p>

<h2>Avec l&rsquo;Amour de Dieu</h2>

<p>Mais avec Dieu dans nos vies, et gr&acirc;ce &agrave; l&#39;habilitation du Saint-Esprit, Dieu nous permet d&#39;&ecirc;tre diff&eacute;rents de ce que nous sommes naturellement. Il fournit la motivation qui nous manque, la capacit&eacute; de l&#39;amour, la cr&eacute;ativit&eacute; pour montrer notre amour de Dieu. C&#39;est un genre d&#39;amour compl&egrave;tement nouveau.<br />
<br />
<em>Nous pouvons aimer de l&rsquo;amour de Dieu.</em> C&#39;&eacute;tait le genre d&#39;amour de Dieu qui nous a amen&eacute;s &agrave; Christ. C&#39;est ce m&ecirc;me amour qui nous soutient et nous encourage chaque jour. Cela nous permet de servir les autres croyants comme il nous a &eacute;t&eacute; command&eacute;. C&#39;est le m&ecirc;me amour qui am&egrave;ne les autres &agrave; une connaissance salvatrice de J&eacute;sus-Christ.<br />
<br />
Mais comment obtenons-nous l&#39;amour de Dieu dans nos vies? L&rsquo;amour et le Saint-Esprit sont ins&eacute;parables; quand nous le recevons, nous recevons son amour. L&#39;&Eacute;criture nous rappelle: &laquo;&nbsp;l&rsquo;amour de Dieu est r&eacute;pandu dans nos c&oelig;urs par le Saint-Esprit qui nous a &eacute;t&eacute; donn&eacute;.&nbsp;&raquo; (Romains 5:5, LSG). Dieu est Esprit, et le fruit de l&rsquo;Esprit est l&rsquo;amour (Galates 5:22). Lorsque nous sommes dirig&eacute;s par l&rsquo;Esprit, nous sommes remplis de Son amour.<br />
<br />
Ainsi, nous sommes remplis de l&#39;amour de Dieu et pr&ecirc;ts &agrave; aimer le monde avec cet amour remarquable, inconditionnel et sans limite. Mais pouvons-nous faire de cet amour une r&eacute;alit&eacute; pratique dans nos vies? Comment les autres sauront-ils qu&#39;ils sont aim&eacute;s si nous ne pouvons pas leur montrer?</p>

<h2>Aimer par la Foi</h2>

<p><em>Nous aimons par la FOI. </em>Tout sur la vie chr&eacute;tienne est bas&eacute; sur la foi; rien de ce que nous avons re&ccedil;u de Dieu ne nous est parvenu, si ce n&#39;est par la foi. Nous aimons par la foi tout comme nous avons re&ccedil;u notre salut - par la foi. Nous aimons par la foi tout comme nous marchons par la foi. Nous aimons par la foi tout comme nous sommes remplis du Saint-Esprit.<br />
<br />
Y a-t-il une limite? Oui. Apr&egrave;s que nous puissions aimer les autres autant que J&eacute;sus nous aime, nous pouvons nous arr&ecirc;ter. C&#39;est la volont&eacute; de Dieu que nous nous aimions les uns les autres, et Il ne nous demande pas de faire quoi que ce soit qu&#39;Il ne nous permette pas de faire. Il nous est rappel&eacute; dans 1 Jean 5: 14,15 que tout ce que nous demandons, selon Sa volont&eacute;, Il entend et r&eacute;pond. Voulez-vous aimer de l&#39;amour de Dieu? R&eacute;clame simplement Sa promesse en rapport avec Son commandement d&#39;aimer, et prends-la par la foi.<br />
<br />
Un coll&egrave;gue et moi avions eu un d&eacute;saccord. Il m&rsquo;&eacute;tait extr&ecirc;mement difficile de travailler avec lui. Je voulais l&#39;aimer, et je savais qu&#39;on m&#39;avait recommand&eacute; de le faire; pourtant, c&#39;&eacute;tait plus que ce que je pouvais faire. Je ne pouvais pas g&eacute;n&eacute;rer l&#39;amour dont j&#39;avais besoin pour cette personne. Et puis je me suis souvenu de 1 Pierre 5: 7 o&ugrave; l&#39;on me dit de d&eacute;charger mes soucis sur Dieu parce qu&#39;Il prend soin. Dans l&#39;ob&eacute;issance, j&#39;ai confi&eacute; le probl&egrave;me et mon incapacit&eacute; &agrave; le r&eacute;soudre &agrave; Dieu, et r&eacute;clam&eacute; son amour pour cet homme par la foi. Les sentiments de trouble que j&#39;avais entretenus dans mon c&oelig;ur avaient disparu au moment o&ugrave; je consid&eacute;r&eacute; que les probl&egrave;mes sont maintenant entre les mains comp&eacute;tentes de Dieu.<br />
<br />
En quelques heures, quelqu&#39;un a gliss&eacute; une note sous ma porte. A ma grande surprise, c&#39;&eacute;tait une lettre d&#39;excuse inattendue de cet homme avec lequel j&#39;&eacute;tais en d&eacute;saccord. Sans conna&icirc;tre ma d&eacute;cision de l&#39;aimer, lui aussi avait d&eacute;cid&eacute; que l&#39;amour &eacute;tait la r&eacute;ponse. Nous nous sommes rencontr&eacute;s pour le caf&eacute; et la pri&egrave;re, et la communion que nous avons eu cet apr&egrave;s-midi &eacute;tait plus chaleureuse et plus gratifiante que nous n&rsquo;en avions eu.</p>

<h2>Aimez vous-m&ecirc;me</h2>

<p>Faites une liste des gens que vous n&#39;aimez pas, et r&eacute;clamez la promesse de 1 Jean 5: 14,15. Et commencez maintenant &agrave; les aimer par la foi en cette promesse de Dieu.<br />
<br />
Est-ce que vous-vous aimez-vous m&ecirc;me? Peut-&ecirc;tre que vous trouverez votre propre nom sur votre liste. Les v&eacute;rit&eacute;s de 1 Corinthiens 13 (le chapitre entier) s&#39;appliquent aussi bien &agrave; nous-m&ecirc;mes et peuvent &ecirc;tre r&eacute;clam&eacute;es pour nous-m&ecirc;mes par la foi de la m&ecirc;me mani&egrave;re que nous les r&eacute;clamerions pour quelqu&#39;un d&#39;autre. Demandez &agrave; Dieu de vous donner Ses yeux afin que vous puissiez vous voir tel qu&#39;Il vous voit. J&eacute;sus vous aime sans r&eacute;serve, inconditionnellement. Il vous aime tellement qu&#39;il est mort pour vous alors que vous &eacute;tiez encore dans le p&eacute;ch&eacute;, ignorant votre besoin de pardon. Si Lui - Dieu lui-m&ecirc;me - peut vous aimer autant, qui &ecirc;tes-vous pour ne pas &ecirc;tre d&rsquo;accord?<br />
<br />
Priez pour chaque personne sur votre liste, demandant au Saint-Esprit de vous remplir de l&#39;amour de Dieu pour chacun d&#39;entre eux. La prochaine fois que vous rencontrez ou parlez &agrave; quelqu&#39;un sur votre liste, faites appel &agrave; Son amour illimit&eacute;, in&eacute;puisable et irr&eacute;sistible pour eux comme un acte de foi. Attendez-vous &agrave; ce que Dieu travaille &agrave; travers vous par la foi. Attendez-vous &agrave; Lui pour utiliser votre sourire, vos paroles douces, votre patience pour leur exprimer Son amour.<br />
<br />
Essayez cet amour sur chaque &laquo;&nbsp;ennemi&nbsp;&raquo; de votre vie &ndash; toute personne qui vous met en col&egrave;re ou vous ignore, ou vous ennuie, ou vous rabaisse - tout &ecirc;tre humain frustrant que vous connaissez. Ensuite, attendez de voir les r&eacute;sultats. Les hommes et les femmes qui nous entourent n&#39;attendent que nous, d&eacute;sirant &ecirc;tre aim&eacute;s avec l&#39;amour irr&eacute;sistible de Dieu.<br />
<br />
<em>La route vers maison semblait plus longue que d&#39;habitude cette nuit d&#39;avril pluvieuse. L&#39;homme au volant venait d&#39;apprendre le commandement de Dieu d&#39;aimer inconditionnellement comme Dieu Lui-m&ecirc;me aime ses enfants. Et maintenant, avec les essuie-glaces battant une cadence constante, il ne pouvait pas secouer la photo de son propre fils, Wayne.</em><br />
<br />
<em>C&#39;&eacute;tait un argument stupide ... dr&ocirc;le, il ne pouvait m&ecirc;me pas se rappeler de quoi ils s&#39;&eacute;taient disput&eacute;s. Mais Wayne &eacute;tait parti de la maison, et il n&#39;avait plus eu de nouvelles de son fils depuis. Cela faisait des mois maintenant, et il ne savait pas si son fils &eacute;tait mort ou vivant. La nostalgie qui &eacute;tait en lui grandissait. &laquo;&nbsp;Oh, mon Dieu,&nbsp;&raquo; cria-t-il dans l&#39;obscurit&eacute;, &quot;je ne croirai pas que Wayne est mort. Tu sais que j&#39;ai besoin d&rsquo;arranger les choses avec lui. Malgr&eacute; tout, je veux lui dire que je l&#39;aime. &raquo;Les larmes se fray&egrave;rent un passage sur ses joues et disparurent dans sa barbe grisonnante. &laquo;&nbsp;S&#39;il te pla&icirc;t, P&egrave;re,&nbsp;&raquo; murmura-t-il d&#39;une voix rauque, &laquo;&nbsp;laisse-moi dire &agrave; mon fils combien je l&#39;aime.&nbsp;&raquo;</em><br />
<br />
<em>Il tourna le coin et jeta un coup d&#39;&oelig;il &agrave; la maison. Pouvait-il voir des choses? La lumi&egrave;re qui est dans la chambre de Wayne &eacute;tait allum&eacute;e. Cela pouvait seulement signifier que son gar&ccedil;on &eacute;tait de retour. Laissant la voiture dans l&#39;all&eacute;e, il se pr&eacute;cipita par une averse dans la maison. &laquo;&nbsp;Wayne&nbsp;&raquo;, appela-t-il. &laquo;&nbsp;Mon fils, c&#39;est toi&nbsp;&raquo;?</em><br />
<br />
<em>Dans les premi&egrave;res heures de la matin&eacute;e, le p&egrave;re et le fils se sont parl&eacute;. &laquo;&nbsp;J&#39;avais tellement peur de rentrer &agrave; la maison, papa,&nbsp;&raquo; dit le gar&ccedil;on. &laquo;&nbsp;Vous avez tous les droits de me d&eacute;tester.&nbsp;&raquo;</em><br />
<br />
<em>&laquo;&nbsp;Je ne te d&eacute;teste pas, mon fils,&nbsp;&raquo; dit le p&egrave;re. &laquo;&nbsp;Dieu et moi t&#39;aimons tel que tu es.&nbsp;&raquo; Le p&egrave;re et le fils se sont embrass&eacute;s. Nous allons le faire. Toi, moi ... et Dieu</em><br />
<br />
Comme c&#39;est formidable d&#39;avoir une force aussi dynamique et joyeuse &agrave; notre disposition! Et tout cela vient de notre tendre Sauveur, J&eacute;sus-Christ. Il promet que tout ce dont nous avons besoin est &agrave; notre disposition dans Sa Parole. Nous n&#39;avons pas besoin de deviner, ni d&#39;esp&eacute;rer, ni de souhaiter; nous avons seulement besoin de r&eacute;clamer son amour par la foi, en ce moment.<br />
<br />
M&eacute;morisez et r&eacute;clamez 1 Corinthiens 13 et demandez au Seigneur de cimenter la v&eacute;rit&eacute; qui s&rsquo;y trouve dans votre vie de jour en jour en puisant, par la foi, des ressources illimit&eacute;es de l&#39;amour qui vous appartiennent par le Saint-Esprit. Cela a chang&eacute; la vie de millions de personnes. Laissez-le changer la v&ocirc;tre en faisant la pri&egrave;re suivante:<br />
<br />
<em>Seigneur, qui t&#39;appelle &laquo;&nbsp;Amour&nbsp;&raquo;, je choisis d&#39;ob&eacute;ir &agrave; Ton commandement d&#39;aimer comme Toi. Je r&eacute;clame ta promesse de me permettre d&#39;aimer par la foi, et je te fais confiance pour m&rsquo;habiliter de l&#39;amour parfait de Ton Saint-Esprit.</em></p>

<h2>Application</h2>

<ol>
	<li>Qu&rsquo;avez-vous aim&eacute; le plus (qu&rsquo;est-ce qui a retenu votre attention)?</li>
	<li>Pourquoi?</li>
	<li>A qui devrais-je transmettre cette information ?</li>
</ol>

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


<p>Adapt&eacute; de Les Messages Transmissibles par Bill Bright. &copy; Cru. Tous droits r&eacute;serv&eacute;s</p>


<!-- begin sdcard languageFooterSingle -->
<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social"  @click="share('android', 'fra', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Comment Aimer par la Foi: ', '/content/M2/fra/tc/ct08.html')">
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