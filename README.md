# webDevAlfa-2018-slides
Slides

Blade do projeto - Site
#site/templates/master.blade.php

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Blog WebDevAlfa</title>

		<!--Bootstrap-->
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">

		<!--CSS Person-->
		<link rel="stylesheet" href="css/webdevalfa.css">

		<!--CSS Person-->
		<link rel="stylesheet" href="css/webdevalfa-reset.css">

		<!--CSS Person-->
		<link rel="stylesheet" href="css/webdevalfa-responsive.css">

		<!--Favicon-->
		<link rel="icon" type="image/png" href="imgs/favicon.png">
	</head>
<body>
	
	<header class="top">
		<div class="container">
			<div class="logo col-md-6">
				<a href="?pg=home">
					<img src="imgs/logo-webdevalfa.png" alt="WebDevAlfa" class="logo">
				</a>
			</div>

			<div class="form col-md-6">
				<form class="form form-search form-inline">
					<input type="text" name="pesquisar" placeholder="Pesquisar?" class="form-control">

					<button>
						<span class="glyphicon glyphicon-search"></span>
					</button>
				</form>
			</div>
		</div><!--End Container-->
	</header><!--End Header TOP-->


	<div class="menu">
		<div class="container container-fluid">
          <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
              <span class="sr-only">Toggle navigation</span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
            </button>
          </div>

          <div id="navbar" class="navbar-collapse collapse">
            <ul class="nav navbar-nav">
              <li><a href="/">Home</a></li>

              <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Categorias <span class="caret"></span></a>
                <ul class="dropdown-menu">
                  <li><a href="/categoria">PHP</a></li>
                  <li><a href="/categoria">JavaScript</a></li>
                  <li><a href="/categoria">jQuery</a></li>
                  <li><a href="/categoria">Ajax</a></li>
                  <li><a href="/categoria">SEO</a></li>
                </ul>
              </li>

              <li><a href="/empresa">Empresa</a></li>
              <li><a href="/contato">Contato</a></li>
              
            </ul>

          </div><!--/.nav-collapse -->
        </div>
	</div><!--End Menu-->


	<div class="container">
		
	@yield('conteudo')

	</div><!--End Container-->


	<footer class="footer">
		<p class="footer">Todos os direitos reservados - WebDevAlfa <?=date('Y')?></p>
	</footer>


	<!--jQuery-->
	<script src="js/jquery-3.1.1.min.js"></script>

	<!--Bootstrap .js-->
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>
</body>
</html>

#--- End Blade: master.blade.php

#site/index.blade.php

@extends('site.templates.master')
@section('conteudo')

<div class="slide">
    <div class="col-md-8">
        <article class="img-big">
            <a href="" title="">
                <img src="imgs/img1.jpg" alt="" class="img-slide-big">

                <h1 class="text-slide">
                    Uma nova maneira de trabalhar com HTML5 - Acesse o Curso HTML5
                </h1>
            </a>
        </article>
    </div>

    <div class="col-md-4">
        <article class="img-small col-md-12 col-sm-6 col-xm-12">
            <a href="" title="">
                <img src="imgs/img2.jpg" alt="" class="img-slide-small">

                <h1 class="text-slide">
                    Um nome para o titulo aqui
                </h1>
            </a>
        </article>
        <article class="img-small col-md-12 col-sm-6 col-xm-12">
            <a href="" title="">
                <img src="imgs/img3.jpg" alt="" class="img-slide-small">
                <h1 class="text-slide">
                    O título do post pode vir bem aqui...
                </h1>
            </a>
        </article>
    </div>
</div><!--Slide-->


<section class="content">
    <div class="col-md-8">
        
        <?php for($i = 1; $i <= 10; $i++){?>
        <article class="post">
            <div class="image-post col-md-4 text-center">
                <img src="imgs/img1.jpg" alt="Nome Post" class="img-post">
            </div>
            <div class="description-post col-md-8">
                <h2 class="title-post">Título do post pode vir bem aqui...</h2>

                <p class="description-post">
                    Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração...
                </p>

                <a class="btn-post" href="?pg=post">Ir <span class="glyphicon glyphicon-chevron-right"></span></a>
            </div>
        </article>
        <?php }?>

        <div class="pagination-posts">
            <nav aria-label="Page navigation">
              <ul class="pagination">
                <li>
                  <a href="#" aria-label="Previous">
                    <span aria-hidden="true">&laquo;</span>
                  </a>
                </li>
                <li class="active"><a href="#">1</a></li>
                <li><a href="#">2</a></li>
                <li><a href="#">3</a></li>
                <li><a href="#">4</a></li>
                <li><a href="#">5</a></li>
                <li>
                  <a href="#" aria-label="Next">
                    <span aria-hidden="true">&raquo;</span>
                  </a>
                </li>
              </ul>
            </nav>
        </div>

    </div><!--POSTS-->

    <!--Sidebar-->
    <div class="col-md-4">
    <iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FfaculdadeAlfaUmuarama%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=316115088513380" width="340" height="500" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>		</section>

@endsection

#--- End Blade: index.blade.php

#site/pages/categoria.blade.php

@extends('site.templates.master')
@section('conteudo')

<div class="category">
	
	<section class="content">
		<div class="col-md-8">

			<div class="title-category">
				<h1 class="title-category">Nome da Categoria</h1>
			</div>
			
			<?php for($i = 1; $i <= 10; $i++){?>
			<article class="post">
				<div class="image-post col-md-4 text-center">
					<img src="imgs/img1.jpg" alt="Nome Post" class="img-post">
				</div>
				<div class="description-post col-md-8">
					<h2 class="title-post">Título do post pode vir bem aqui...</h2>

					<p class="description-post">
						Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração...
					</p>

					<a class="btn-post" href="/post">Ir <span class="glyphicon glyphicon-chevron-right"></span></a>
				</div>
			</article>
			<?php }?>

			<div class="pagination-posts">
				<nav aria-label="Page navigation">
				  <ul class="pagination">
				    <li>
				      <a href="#" aria-label="Previous">
				        <span aria-hidden="true">&laquo;</span>
				      </a>
				    </li>
				    <li class="active"><a href="#">1</a></li>
				    <li><a href="#">2</a></li>
				    <li><a href="#">3</a></li>
				    <li><a href="#">4</a></li>
				    <li><a href="#">5</a></li>
				    <li>
				      <a href="#" aria-label="Next">
				        <span aria-hidden="true">&raquo;</span>
				      </a>
				    </li>
				  </ul>
				</nav>
			</div>

		</div><!--POSTS-->

		<!--Sidebar-->
		<div class="col-md-4 text-center">
		<iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FfaculdadeAlfaUmuarama%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=316115088513380" width="340" height="500" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>		</div><!--Sidebar-->
	</section>

</div>

@endsection
       
#--- End Blade: categoria.blade.php

#site/pages/contato.blade.php

@extends('site.templates.master')
@section('conteudo')

<div class="contact text-center">
	<h1 class="title">Entre em Contato</h1>
	<h2 class="sub-title">Tenha todas as suas Dúvidas esclarecidas pela nossa equipe.</h2>

	<form class="form form-contact">
		<input type="text" name="nome" placeholder="Nome:">
		<input type="email" name="email" placeholder="E-mail:">
		<input type="text" name="assunto" placeholder="Assunto:">
		<textarea placeholder="Mensagem:" name="mensagem"></textarea>

		<button class="btn-contact">Enviar</button>
	</form>
</div>

@endsection
       
#--- End Blade: contato.blade.php

#site/pages/empresa.blade.php

@extends('site.templates.master')
@section('conteudo')

<div class="conpany text-center">
	<h1 class="title">
		Sobre a Faculdade Alfa
	</h1>
	<h2 class="sub-title">
			A Faculdade de Tecnologia ALFA de Umuarama, sustentada pela experiência de seus mantenedores, já atuantes na prestação de serviços educacionais há mais de vinte e cinco anos, tem como um de seus objetivos dar continuidade ao ensino com qualidade e contribuir com a formação de profissionais para o mercado de trabalho.
		Sempre atenta às mudanças e às necessidades de novas tecnologias e exigências de especialistas visa promover grandes possibilidades de ingresso no mercado empresarial.
		A Faculdade de Tecnologia ALFA conta com uma equipe de professores qualificados, com experiência no ensino superior e no mercado de trabalho garantindo ao aluno o conhecimento necessário, responsabilidade e infra-estrutura adequada para alcançar o que há de melhor em sua área.
	</h2>

	<div class="col-md-6">
		<img src="imgs/empresa-webdevalfa.jpg" alt="Faculdade Akfa" class="company">
	</div>
	<div class="col-md-6 text-company text-justify">
		<p class="text-company-esp">Objetivos </br>
			Aliar informação com formação: garantir que os alunos tenham tanto o embasamento científico, fundamentação teórica, quanto o técnico, aplicabilidade na prática.
			Formular programas que incorporem a identificação das competências críticas empresariais e humanas e reflitam o compromisso com a cidadania empresarial.
			Introduzir modelos comportamentais voltados para o aprendizado permanente, de forma a proporcionar a contínua atualização dos conhecimentos. Oferecer cursos de acordo com o que o mercado pede, sendo isto identificado através de pesquisas.
			Estender à comunidade as atividades acadêmicas, visando a elevação do nível sócio-econômico-cultural.
			Promover o ambiente interno de desenvolvimento de relações interpessoais, propiciando o crescimento integrado do ser humano e o pleno exercício de suas habilidades e potencialidades.
		</p>
		<p>Missão</br>
			Constituir-se em centro de excelência no campo do ensino superior, construindo uma educação comprometida com a ética, a cidadania e o conhecimento, resultando na formação de profissionais aptos a contribuírem no desenvolvimento da sociedade.
		</p>
		<p>Finalidades</br>
		Fundamentada na sua filosofia, a Faculdade ALFA de Umuarama tem por finalidade a solidificação das diretrizes curriculares emanadas do Ministério da Educação cumprindo os princípios didático-pedagógicos para os seus cursos. Essas diretrizes solidificarão a excelência das práticas acadêmicas a serem desenvolvidas no decorrer das graduações da Faculdade.</p>
		</p>
	</div>
</div>
@endsection
       
#--- End Blade: empresa.blade.php

#site/pages/post.php

@extends('site.templates.master')
@section('conteudo')

<div class="category">
	
	<section class="content">
		<div class="col-md-8">
			
			<article class="post">
				<div class="image-post text-center">
					<img src="imgs/img1.jpg" alt="Nome Post" class="img-post">
				</div>
				<div class="description-post-pg text-justify">
					<p class="details-post">
						<span>Autor:</span> Jaime Vendrame / <span>Data publicação</span>: <time datetime="">01/09/2018</time>	
					</p>

					<h2 class="title-post-pg">Título do post pode vir bem aqui...</h2>

					<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>

					<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>

					<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>

					<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
				</div>
			</article><!--End Post-->

			<article class="post comments">
				<h2 class="title-comment">Deixe o seu comentário</h2>
				<form class="form form-contact form-comment">
					<input type="name" name="nome" placeholder="Nome:">
					<input type="email" name="email" placeholder="E-mail:">
					<textarea name="descricao" placeholder="Descrição"></textarea>

					<button>Enviar</button>
				</form>

				<div class="comment">
					<div class="col-md-2 text-center">
						<img src="imgs/no-image.png" alt="Jaime Vendrame" class="user-comment-img img-circle">
					</div>
					<div class="col-md-10 comment-user">
						<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
					</div>
				</div>

				<div class="comment">
					<div class="col-md-2 text-center">
						<img src="imgs/no-image.png" alt="Jaime Vendrame" class="user-comment-img img-circle">
					</div>
					<div class="col-md-10 comment-user">
						<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
					</div>
				</div>
				<div class="reply-comment">
					<div class="col-md-2 text-center">
						<img src="imgs/no-image.png" alt="Jaime Vendrame" class="user-comment-img img-circle">
					</div>
					<div class="col-md-10 comment-user">
						<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
					</div>
				</div>
				<div class="reply-comment">
					<div class="col-md-2 text-center">
						<img src="imgs/no-image.png" alt="Jaime Vendrame" class="user-comment-img img-circle">
					</div>
					<div class="col-md-10 comment-user">
						<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
					</div>
				</div>

				<div class="comment">
					<div class="col-md-2 text-center">
						<img src="imgs/no-image.png" alt="Jaime Vendrame" class="user-comment-img img-circle">
					</div>
					<div class="col-md-10 comment-user">
						<p>Lorem Ipsum é simplesmente uma simulação de texto da indústria tipográfica e de impressos, e vem sendo utilizado desde o século XVI, quando um impressor desconhecido pegou uma bandeja de tipos e os embaralhou para fazer um livro de modelos de tipos. Lorem Ipsum sobreviveu não só a cinco séculos, como também ao salto para a editoração eletrônica, permanecendo essencialmente inalterado. Se popularizou na década de 60, quando a Letraset lançou decalques contendo passagens de Lorem Ipsum, e mais recentemente quando passou a ser integrado a softwares de editoração eletrônica como Aldus PageMaker.</p>
					</div>
				</div>
			</article>


		</div><!--POSTS-->

		<!--Sidebar-->
		<div class="col-md-4">
		<iframe src="https://www.facebook.com/plugins/page.php?href=https%3A%2F%2Fwww.facebook.com%2FfaculdadeAlfaUmuarama%2F&tabs=timeline&width=340&height=500&small_header=false&adapt_container_width=true&hide_cover=false&show_facepile=true&appId=316115088513380" width="340" height="500" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>		</div><!--Sidebar-->
	</section>


	<section class="post-relation">
		<h1 class="title-post-rel">Posts Relacionados:</h1>

		<?php for($i = 1; $i <= 4; $i++){?>
			<article class="post-rel col-md-3 col-xm-6 col-sm-12">
				<a href="">
					<div class="image-post text-center">
						<img src="imgs/img1.jpg" alt="Nome Post" class="img-post">
					</div>
					<div class="description-post">
						<h2 class="title-post-rel-list">Título do post pode vir bem aqui...</h2>
					</div>
				</a>
			</article>
			<?php }?>
	</section>

</div>

@endsection
       
#--- End Blade: post.blade.php

