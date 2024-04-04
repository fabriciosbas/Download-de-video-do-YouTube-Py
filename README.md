## Célula de teste - DOWNLOAD CONFIRMADO! download direto no PC

import youtube_dl
from pytube import YouTube

def download_video(video_url, output_path):
    try:
        # Cria uma instância do objeto YouTube com o URL do vídeo
        yt = YouTube(video_url)

        # Seleciona o formato de vídeo com a melhor qualidade
        video = yt.streams.get_highest_resolution()

        # Faz o download do vídeo para o caminho especificado
        video.download(output_path)
        print("Download completo!")

    except Exception as e:
        print("Ocorreu um erro durante o download:", str(e))

if __name__ == "__main__":
    video_url = input("Insira o URL do vídeo do YouTube")
    output_path = "C:\\Users\\Fabrício\\Downloads" #COLOCAR O CAMINHO QUE VC QUER SALVAR O VIDEO#
    
    download_video(video_url, output_path)
