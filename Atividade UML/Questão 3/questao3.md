``` Mermaid
    classDiagram
    class Anuncio{
    - Date data_anuncio
    - Float valor_anuncio
    - String titulo_anuncio
    - String contato_anuncio
    - String tel_anuncio1
    - String tel_anuncio2
    - String obs_anuncio
    + get_obsAnuncio() String
    + get_valorAnuncio() Float
    + get_dataAnuncio() Date
    - Secao.get_secaoProd()
    + cadastroAnuncio(valor_anuncio, titulo_anuncio, contato_anuncio, tel_anuncio1, tel_anuncio2, obs_anuncio)
    }
    class Cliente{
        - Enum cli_interesses
        - String cli_email
        - String cli_nome
        - Int cod_anunciante
        + get_codAnunciante() Int
        + set_codAnunciante()
        + cad_cliente(cli_interesses, cli_email, cli_nome)
    }
    class TipoAnuncio{
        - Enum tipo_anuncio
        - Int qtd_palavra
        - URL imagem_prod
        - bool have_image
        + temImg() bool
        + get_img() URL
        + set_img()
        + set_tipo()
    }
    class Secao{
        - Enum secao_prod
        + get_secaoProd() Enum
        + set_secaoProd()
        + enviarEmail()
    }
    class EmailOferta{
        Anuncio.get_obsAnuncio()
        Anuncio.get_valorAnuncio()
        Anuncio.get_dataAnuncio()
    }

Anuncio -->"1" TipoAnuncio
Anuncio -->"*" Secao
Cliente -->"*" Anuncio
Cliente -->"*" EmailOferta
EmailOferta -->"*" Anuncio

```