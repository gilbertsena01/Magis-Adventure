import React, { useState, useEffect } from 'react';
import { Sword, Shield, Book, Target, Crown, Scroll, Hammer, User, Trophy, Clock } from 'lucide-react';

const MagistraturaRPG = () => {
  // Estado inicial do jogador
  const [jogador, setJogador] = useState({
    nome: "Gilbert Sena",
    nivel: 1,
    vida: 100,
    xp: 0,
    pomodoros: 0,
    cimitarras: 0,
    equipamentos: {
      pomodoro: "Pomodoro de Bronze",
      cimitarra: "Cimitarra de Ferro"
    },
    conquistas: [],
    disciplinasFoco: []
  });

  // Boss da semana atual
  const [bossAtual, setBossAtual] = useState(0);
  const [semana, setSemana] = useState(1);

  // Progresso diário
  const [progressoDiario, setProgressoDiario] = useState({
    pomodoros: 0,
    questoes: 0,
    metaPomodorosAtingida: false,
    metaQuestoesAtingida: false
  });

  // Imagens dos bosses em base64 (versões otimizadas)
  const imagensBosses = [
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNEQTg1MjEiLz48cGF0aCBkPSJNMzAgMjBINzBWODBIMzBWMjBaIiBmaWxsPSIjRkZEQTAwIi8+PHBhdGggZD0iTTQwIDMwSDYwVjcwSDQwVjMwWiIgZmlsbD0iIzk5OTk5OSIvPjwvc3ZnPg==", // Constitucio
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMxMTExMTEiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjQwIiByPSIxNSIgZmlsbD0iIzk5OTk5OSIvPjxwYXRoIGQ9Ik00MCA2MEg2MFY4MEg0MFY2MFoiIGZpbGw9IiM2NjY2NjYiLz48L3N2Zz4=", // Criminus Rex
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMyMjIyMjIiLz48cG9seWdvbiBwb2ludHM9IjUwLDMwIDYwLDQwIDUwLDUwIDQwLDQwIiBmaWxsPSIjRkZEQTAwIi8+PGNpcmNsZSBjeD0iNTAiIGN5PSI2NSIgcj0iMTAiIGZpbGw9IiM5OTk5OTkiLz48L3N2Zz4=", // Processus
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNEQzI2MjYiLz48cmVjdCB4PSIzMCIgeT0iNDAiIHdpZHRoPSI0MCIgaGVpZ2h0PSIyMCIgZmlsbD0iI0ZGRkZGRiIvPjx0ZXh0IHg9IjUwIiB5PSI1NSIgZm9udC1zaXplPSI4IiBmaWxsPSIjMDAwIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj5WT1RPPC90ZXh0Pjwvc3ZnPg==", // Electoralis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMzMzMzMzMiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iIzk5OTk5OSIvPjxyZWN0IHg9IjM1IiB5PSI1MCIgd2lkdGg9IjMwIiBoZWlnaHQ9IjMwIiBmaWxsPSIjNjY2NjY2Ii8+PC9zdmc+", // Administratus
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiM4QjQ1MTMiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjQwIiByPSIxNSIgZmlsbD0iI0ZGRkZGRiIvPjxyZWN0IHg9IjM1IiB5PSI2MCIgd2lkdGg9IjMwIiBoZWlnaHQ9IjIwIiBmaWxsPSIjRkZGRkZGIi8+PC9zdmc+", // Civis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiM0Qjc3QkUiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iI0ZGRkZGRiIvPjxwYXRoIGQ9Ik0zNSA1MEw2NSA1MEw2NSA3MEwzNSA3MFoiIGZpbGw9IiNGRkRBMDAiLz48L3N2Zz4=", // Processus Civilis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMwMzY5QTAiLz48Y2lyY2xlIGN4PSI0NSIgY3k9IjM1IiByPSI4IiBmaWxsPSIjRkZEQTAwIi8+PGNpcmNsZSBjeD0iNjAiIGN5PSI2NSIgcj0iNSIgZmlsbD0iI0ZGREEwMCIvPjxwYXRoIGQ9Ik0zNSA1MEw2NSA1MEw2NSA3MEwzNSA3MFoiIGZpbGw9IiM5OTk5OTkiLz48L3N2Zz4=", // Juvenis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNFQTU4MEMiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjQwIiByPSIxMiIgZmlsbD0iIzk5OTk5OSIvPjxyZWN0IHg9IjQwIiB5PSI1NSIgd2lkdGg9IjIwIiBoZWlnaHQ9IjE1IiBmaWxsPSIjRkZEQTAwIi8+PHRleHQgeD0iNTAiIHk9IjY4IiBmb250LXNpemU9IjEwIiBmaWxsPSIjMDAwIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj4kPC90ZXh0Pjwvc3ZnPg==", // Tributarius
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMxNDUzNTYiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iIzk5OTk5OSIvPjxyZWN0IHg9IjM1IiB5PSI1NSIgd2lkdGg9IjMwIiBoZWlnaHQ9IjIwIiBmaWxsPSIjRkZEQTAwIi8+PGNpcmNsZSBjeD0iNTAiIGN5PSI2NSIgcj0iOCIgZmlsbD0iIzk5OTk5OSIvPjwvc3ZnPg==", // Empresarius
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMwNTk2NjkiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxNSIgZmlsbD0iIzIyQzU1RSIvPjxwYXRoIGQ9Ik00MCA1MEw2MCA1MEw1NSA2NUw0NSA2NVoiIGZpbGw9IiM4Qjc5NTUiLz48Y2lyY2xlIGN4PSI1MiIgY3k9IjcwIiByPSI2IiBmaWxsPSIjMjJDNTVFIi8+PC9zdmc+", // Ambientalis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiMwOTkxQTYiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iI0ZGRkZGRiIvPjxyZWN0IHg9IjM1IiB5PSI1NSIgd2lkdGg9IjMwIiBoZWlnaHQ9IjE1IiBmaWxsPSIjMzY0OEFBIi8+PGNpcmNsZSBjeD0iNDAiIGN5PSI2NSIgcj0iNCIgZmlsbD0iI0ZGRkZGRiIvPjxjaXJjbGUgY3g9IjYwIiBjeT0iNjUiIHI9IjQiIGZpbGw9IiNGRkZGRkYiLz48L3N2Zz4=", // Internationalis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNEQjI3NzciLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iIzk5OTk5OSIvPjxyZWN0IHg9IjM1IiB5PSI1NSIgd2lkdGg9IjMwIiBoZWlnaHQ9IjIwIiBmaWxsPSIjRkZGRkZGIi8+PGNpcmNsZSBjeD0iNDUiIGN5PSI2NSIgcj0iMyIgZmlsbD0iI0ZGREEwMCIvPjxjaXJjbGUgY3g9IjU1IiBjeT0iNjUiIHI9IjMiIGZpbGw9IiNGRkRBMDAiLz48L3N2Zz4=", // Previdencialis
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiM4QjVDRjYiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iIzk5OTk5OSIvPjxwYXRoIGQ9Ik0zNSA1NUw0NSA1MEw1NSA1MEw2NSA1NUw2MCA2NUw0MCA2NVoiIGZpbGw9IiNGRkRBMDAiLz48dGV4dCB4PSI1MCIgeT0iNzUiIGZvbnQtc2l6ZT0iOCIgZmlsbD0iI0ZGRiIgdGV4dC1hbmNob3I9Im1pZGRsZSI+JCQkPC90ZXh0Pjwvc3ZnPg==", // Economicus
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNGMzY4QTciLz48Y2lyY2xlIGN4PSI0NSIgY3k9IjM1IiByPSI4IiBmaWxsPSIjRkZGRkZGIi8+PGNpcmNsZSBjeD0iNTgiIGN5PSI0NSIgcj0iNiIgZmlsbD0iI0ZGRkZGRiIvPjxyZWN0IHg9IjM1IiB5PSI1NSIgd2lkdGg9IjMwIiBoZWlnaHQ9IjI1IiBmaWxsPSIjRkZEQTAwIi8+PHRleHQgeD0iNTAiIHk9IjcwIiBmb250LXNpemU9IjgiIGZpbGw9IiMwMDAiIHRleHQtYW5jaG9yPSJtaWRkbGUiPkNBUlQ8L3RleHQ+PC9zdmc+", // Consumidor
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiNGNTk3MTciLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxNSIgZmlsbD0iI0ZGRkZGRiIvPjxyZWN0IHg9IjM4IiB5PSI1NSIgd2lkdGg9IjI0IiBoZWlnaHQ9IjE1IiBmaWxsPSIjOEI3OTU1Ii8+PHRleHQgeD0iNTAiIHk9IjgwIiBmb250LXNpemU9IjEwIiBmaWxsPSIjRkZGIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIj7OqjwvdGV4dD48L3N2Zz4=", // Humanitas
    "data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHJlY3Qgd2lkdGg9IjEwMCIgaGVpZ2h0PSIxMDAiIGZpbGw9IiM4NENDMTYiLz48Y2lyY2xlIGN4PSI1MCIgY3k9IjM1IiByPSIxMiIgZmlsbD0iI0ZGRkZGRiIvPjxwYXRoIGQ9Ik0zNSA1MEw2NSA1MEw2MCA2NUw0MCA2NVoiIGZpbGw9IiNGRkRBMDAiLz48Y2lyY2xlIGN4PSI0NSIgY3k9IjcwIiByPSI0IiBmaWxsPSIjRkY2NjY2Ii8+PGNpcmNsZSBjeD0iNTUiIGN5PSI3MCIgcj0iNCIgZmlsbD0iI0ZGNjY2NiIvPjwvc3ZnPg==" // Protector Humanus
  ];

  // Bosses das disciplinas
  const bosses = [
    {
      nome: "Constitucio, O Guardião dos Direitos",
      disciplina: "Direito Constitucional",
      vida: 400,
      vidaAtual: 400,
      descricao: "Protetor supremo da Carta Magna, mestre dos princípios fundamentais",
      cor: "bg-blue-600",
      habilidade: "Controle de Constitucionalidade",
      imagem: imagensBosses[0]
    },
    {
      nome: "Criminus Rex, O Senhor das Sombras",
      disciplina: "Direito Penal",
      vida: 450,
      vidaAtual: 450,
      descricao: "Imperador do crime e castigo, conhece todos os tipos penais",
      cor: "bg-red-600",
      habilidade: "Tipificação Penal",
      imagem: imagensBosses[1]
    },
    {
      nome: "Processus, O Mestre dos Ritos",
      disciplina: "Direito Processual Penal",
      vida: 420,
      vidaAtual: 420,
      descricao: "Guardião dos procedimentos penais, senhor da persecução",
      cor: "bg-purple-600",
      habilidade: "Prisão Processual",
      imagem: imagensBosses[2]
    },
    {
      nome: "Electoralis, O Senhor da Democracia",
      disciplina: "Direito Eleitoral",
      vida: 350,
      vidaAtual: 350,
      descricao: "Guardião das urnas e da soberania popular, mestre das eleições",
      cor: "bg-indigo-700",
      habilidade: "Propaganda Eleitoral",
      imagem: imagensBosses[3]
    },
    {
      nome: "Administratus, O Burocrata Supremo",
      disciplina: "Direito Administrativo",
      vida: 380,
      vidaAtual: 380,
      descricao: "Regente do Estado, mestre dos atos administrativos",
      cor: "bg-green-600",
      habilidade: "Poder de Polícia",
      imagem: imagensBosses[4]
    },
    {
      nome: "Civis, O Patriarca das Relações",
      disciplina: "Direito Civil",
      vida: 400,
      vidaAtual: 400,
      descricao: "Ancião das relações privadas, guardião dos contratos",
      cor: "bg-yellow-600",
      habilidade: "Responsabilidade Civil",
      imagem: imagensBosses[5]
    },
    {
      nome: "Processus Civilis, O Mestre da Justiça",
      disciplina: "Direito Processual Civil",
      vida: 450,
      vidaAtual: 450,
      descricao: "Senhor dos procedimentos civis, guardião do devido processo",
      cor: "bg-indigo-600",
      habilidade: "Tutela de Urgência",
      imagem: imagensBosses[6]
    },
    {
      nome: "Juvenis, O Protetor dos Pequenos",
      disciplina: "Direito da Criança e Adolescente",
      vida: 320,
      vidaAtual: 320,
      descricao: "Guardião da infância e juventude, defensor da proteção integral",
      cor: "bg-sky-600",
      habilidade: "Medidas Socioeducativas",
      imagem: imagensBosses[7]
    },
    {
      nome: "Tributarius, O Cobrador Eterno",
      disciplina: "Direito Tributário",
      vida: 350,
      vidaAtual: 350,
      descricao: "Senhor dos impostos, mestre da capacidade contributiva",
      cor: "bg-orange-600",
      habilidade: "Lançamento Tributário",
      imagem: imagensBosses[8]
    },
    {
      nome: "Empresarius, O Magnata Jurídico",
      disciplina: "Direito Empresarial",
      vida: 320,
      vidaAtual: 320,
      descricao: "Rei dos negócios, guardião da livre iniciativa",
      cor: "bg-teal-600",
      habilidade: "Recuperação Judicial",
      imagem: imagensBosses[9]
    },
    {
      nome: "Ambientalis, O Protetor da Natureza",
      disciplina: "Direito Ambiental",
      vida: 300,
      vidaAtual: 300,
      descricao: "Guardião verde, defensor do meio ambiente equilibrado",
      cor: "bg-emerald-600",
      habilidade: "Princípio da Precaução",
      imagem: imagensBosses[10]
    },
    {
      nome: "Internationalis, O Diplomata Supremo",
      disciplina: "Direito Internacional",
      vida: 280,
      vidaAtual: 280,
      descricao: "Mestre das relações entre nações, guardião dos tratados",
      cor: "bg-cyan-600",
      habilidade: "Soberania Jurídica",
      imagem: imagensBosses[11]
    },
    {
      nome: "Previdencialis, O Protetor Social",
      disciplina: "Direito Previdenciário",
      vida: 300,
      vidaAtual: 300,
      descricao: "Guardião da seguridade social, mestre dos benefícios",
      cor: "bg-pink-600",
      habilidade: "Carência Previdenciária",
      imagem: imagensBosses[12]
    },
    {
      nome: "Economicus, O Regulador dos Mercados",
      disciplina: "Direito Econômico",
      vida: 280,
      vidaAtual: 280,
      descricao: "Senhor da ordem econômica, guardião da concorrência",
      cor: "bg-violet-600",
      habilidade: "Defesa da Concorrência",
      imagem: imagensBosses[13]
    },
    {
      nome: "Consumidor, O Protetor dos Vulneráveis",
      disciplina: "Direito do Consumidor",
      vida: 250,
      vidaAtual: 250,
      descricao: "Defensor dos hipossuficientes, mestre das relações de consumo",
      cor: "bg-rose-600",
      habilidade: "Inversão do Ônus da Prova",
      imagem: imagensBosses[14]
    },
    {
      nome: "Humanitas, O Sábio Filósofo",
      disciplina: "Formação Humanística",
      vida: 350,
      vidaAtual: 350,
      descricao: "Ancião da sabedoria, guardião da ética e filosofia jurídica",
      cor: "bg-amber-600",
      habilidade: "Hermenêutica Jurídica",
      imagem: imagensBosses[15]
    },
    {
      nome: "Protector Humanus, O Defensor Universal",
      disciplina: "Direitos Humanos",
      vida: 380,
      vidaAtual: 380,
      descricao: "Guardião da dignidade humana, mestre dos direitos fundamentais",
      cor: "bg-lime-600",
      habilidade: "Dignidade da Pessoa Humana",
      imagem: imagensBosses[16]
    }
  ];

  // Equipamentos disponíveis
  const equipamentos = {
    pomodoros: [
      { nome: "Pomodoro de Bronze", dano: 50, nivel: 1 },
      { nome: "Pomodoro de Prata", dano: 65, nivel: 3 },
      { nome: "Pomodoro de Ouro", dano: 80, nivel: 5 },
      { nome: "Pomodoro de Platina", dano: 95, nivel: 8 },
      { nome: "Pomodoro de Diamante", dano: 110, nivel: 12 },
      { nome: "Pomodoro Celestial", dano: 130, nivel: 15 }
    ],
    cimitarras: [
      { nome: "Cimitarra de Ferro", dano: 80, nivel: 1 },
      { nome: "Cimitarra de Aço", dano: 100, nivel: 3 },
      { nome: "Cimitarra de Mithril", dano: 120, nivel: 5 },
      { nome: "Cimitarra de Adamantium", dano: 140, nivel: 8 },
      { nome: "Cimitarra Dracônica", dano: 160, nivel: 12 },
      { nome: "Cimitarra dos Deuses", dano: 200, nivel: 15 }
    ]
  };

  // Verificar evolução de equipamentos
  const verificarEvolucaoEquipamentos = () => {
    const novoPomodoro = equipamentos.pomodoros.find(eq => 
      eq.nivel <= jogador.nivel && eq.dano > equipamentos.pomodoros.find(p => p.nome === jogador.equipamentos.pomodoro)?.dano
    );
    
    const novaCimitarra = equipamentos.cimitarras.find(eq => 
      eq.nivel <= jogador.nivel && eq.dano > equipamentos.cimitarras.find(c => c.nome === jogador.equipamentos.cimitarra)?.dano
    );

    if (novoPomodoro || novaCimitarra) {
      setJogador(prev => ({
        ...prev,
        equipamentos: {
          pomodoro: novoPomodoro?.nome || prev.equipamentos.pomodoro,
          cimitarra: novaCimitarra?.nome || prev.equipamentos.cimitarra
        }
      }));
    }
  };

  // Adicionar Pomodoro
  const adicionarPomodoro = () => {
    const novoProgresso = { ...progressoDiario };
    novoProgresso.pomodoros += 1;
    novoProgresso.metaPomodorosAtingida = novoProgresso.pomodoros >= 4;
    
    setProgressoDiario(novoProgresso);
    setJogador(prev => ({ 
      ...prev, 
      pomodoros: prev.pomodoros + 1,
      xp: prev.xp + 10
    }));
  };

  // Adicionar 10 questões (1 Cimitarra)
  const adicionarCimitarra = () => {
    const novoProgresso = { ...progressoDiario };
    novoProgresso.questoes += 10;
    novoProgresso.metaQuestoesAtingida = novoProgresso.questoes >= 20;
    
    setProgressoDiario(novoProgresso);
    setJogador(prev => ({ 
      ...prev, 
      cimitarras: prev.cimitarras + 1,
      xp: prev.xp + 15
    }));
  };

  // Atacar boss com Pomodoro
  const atacarComPomodoro = () => {
    if (jogador.pomodoros <= 0) return;
    
    const equipPomodoro = equipamentos.pomodoros.find(eq => eq.nome === jogador.equipamentos.pomodoro);
    const dano = equipPomodoro.dano;
    
    const novosBosses = [...bosses];
    novosBosses[bossAtual].vidaAtual = Math.max(0, novosBosses[bossAtual].vidaAtual - dano);
    
    setJogador(prev => ({ ...prev, pomodoros: prev.pomodoros - 1, xp: prev.xp + 20 }));
    
    verificarVitoria(novosBosses[bossAtual]);
  };

  // Atacar boss com Cimitarra
  const atacarComCimitarra = () => {
    if (jogador.cimitarras <= 0) return;
    
    const equipCimitarra = equipamentos.cimitarras.find(eq => eq.nome === jogador.equipamentos.cimitarra);
    const dano = equipCimitarra.dano;
    
    const novosBosses = [...bosses];
    novosBosses[bossAtual].vidaAtual = Math.max(0, novosBosses[bossAtual].vidaAtual - dano);
    
    setJogador(prev => ({ ...prev, cimitarras: prev.cimitarras - 1, xp: prev.xp + 30 }));
    
    verificarVitoria(novosBosses[bossAtual]);
  };

  // Verificar vitória contra boss
  const verificarVitoria = (boss) => {
    if (boss.vidaAtual <= 0) {
      setJogador(prev => ({
        ...prev,
        xp: prev.xp + 500,
        nivel: Math.floor((prev.xp + 500) / 1000) + 1,
        conquistas: [...prev.conquistas, `Derrotou ${boss.nome}`]
      }));
      
      // Avançar para próximo boss na próxima semana
      setTimeout(() => {
        proximoBoss();
      }, 2000);
    }
  };

  // Próximo boss
  const proximoBoss = () => {
    setBossAtual((prev) => (prev + 1) % bosses.length);
    setSemana(prev => prev + 1);
    
    // Resetar vida do boss
    const novosBosses = [...bosses];
    novosBosses.forEach(boss => boss.vidaAtual = boss.vida);
  };

  // Reset diário
  const resetDiario = () => {
    setProgressoDiario({
      pomodoros: 0,
      questoes: 0,
      metaPomodorosAtingida: false,
      metaQuestoesAtingida: false
    });
  };

  // Verificar level up
  useEffect(() => {
    const novoNivel = Math.floor(jogador.xp / 1000) + 1;
    if (novoNivel > jogador.nivel) {
      setJogador(prev => ({ ...prev, nivel: novoNivel, vida: 100 + (novoNivel * 20) }));
      verificarEvolucaoEquipamentos();
    }
  }, [jogador.xp]);

  const bossAtualData = bosses[bossAtual];
  const equipPomodoroAtual = equipamentos.pomodoros.find(eq => eq.nome === jogador.equipamentos.pomodoro);
  const equipCimitarraAtual = equipamentos.cimitarras.find(eq => eq.nome === jogador.equipamentos.cimitarra);

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 text-white p-4">
      <div className="max-w-6xl mx-auto">
        {/* Header */}
        <div className="text-center mb-6">
          <h1 className="text-4xl font-bold mb-2 bg-gradient-to-r from-yellow-400 to-orange-500 bg-clip-text text-transparent">
            ⚖️ RPG da Magistratura ⚖️
          </h1>
          <p className="text-lg text-gray-300">Jornada Épica Rumo à Aprovação</p>
        </div>

        {/* Status do Jogador */}
        <div className="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
          <div className="bg-gray-800 rounded-lg p-4">
            <div className="flex items-center mb-4">
              <div className="w-16 h-16 mr-4 rounded-full bg-gray-700 flex items-center justify-center overflow-hidden">
                <img 
                  src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTAwIiBoZWlnaHQ9IjEwMCIgdmlld0JveD0iMCAwIDEwMCAxMDAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSIxMDAiIGhlaWdodD0iMTAwIiBmaWxsPSIjMDAwMDAwIi8+CjxwYXRoIGQ9Ik0yMCA4MEM0MCA2MCA2MCA2MCA4MCA4MEw4MCA5MEw2MCA5MEw0MCA5MEwyMCA5MEwyMCA4MFoiIGZpbGw9IiM5OTk5OTkiLz4KPHA+YXRoIGQ9Ik0zMCA0MEM0MCAzMCA2MCAzMCA3MCA0MEw3MCA2MEw2MCA3MEw0MCA3MEwzMCA2MEwzMCA0MFoiIGZpbGw9IiNEOTUzNDYiLz4KPHA+YXRoIGQ9Ik00MCAyMEM1MCAyMCA2MCAyMCA3MCAzMEw2MCAzNUw1MCAzNUw0MCAzNUwzMCAzNUw0MCAyMFoiIGZpbGw9IiM5OTk5OTkiLz4KPHA+YXRoIGQ9Ik00NSAzNUw0OCAzOEw1MiAzOEw1NSAzNUw1MiAzMkw0OCAzMkw0NSAzNVoiIGZpbGw9IiMzMzMzMzMiLz4KPHA+YXRoIGQ9Ik00MCA1MEw0NSA0NUw1NSA0NUw2MCA1MEw1NSA1NUw0NSA1NUw0MCA1MFoiIGZpbGw9IiNGRkRBMDAiLz4KPHA+YXRoIGQ9Ik0xNSA0NUwyNSAzNUwyNSA0NUwyNSA1NUwxNSA2NUwxNSA0NVoiIGZpbGw9IiNDN0M3QzciLz4KPHA+YXRoIGQ9Ik03NSA0NUw4NSAzNUw4NSA0NUw4NSA1NUw3NSA2NUw3NSA0NVoiIGZpbGw9IiNGRjY2NDciLz4KPC9zdmc+Cg=="
                  alt="Gilbert Sena - Cavaleiro da Justiça"
                  className="w-full h-full object-cover rounded-full"
                  onError={(e) => {
                    e.target.style.display = 'none';
                    e.target.nextSibling.style.display = 'flex';
                  }}
                />
                <div className="w-full h-full bg-gradient-to-br from-red-600 to-yellow-600 rounded-full items-center justify-center text-2xl" style={{display: 'none'}}>
                  ⚖️
                </div>
              </div>
              <div>
                <h3 className="text-xl font-bold">{jogador.nome}</h3>
                <p className="text-sm text-gray-300">Cavaleiro da Justiça</p>
              </div>
            </div>
            <div className="mt-2">
              <p className="text-sm">Nível: <span className="text-yellow-400 font-bold">{jogador.nivel}</span></p>
              <p className="text-sm">XP: <span className="text-green-400">{jogador.xp}</span> / {jogador.nivel * 1000}</p>
              <div className="w-full bg-gray-700 rounded-full h-2 mt-1">
                <div 
                  className="bg-green-500 h-2 rounded-full"
                  style={{ width: `${(jogador.xp % 1000) / 10}%` }}
                ></div>
              </div>
            </div>
          </div>

          <div className="bg-gray-800 rounded-lg p-4">
            <div className="flex items-center mb-2">
              <Target className="w-5 h-5 mr-2 text-orange-400" />
              <h3 className="text-lg font-bold">Arsenal</h3>
            </div>
            <div className="space-y-1">
              <p className="text-sm">🍅 Pomodoros: <span className="text-red-400 font-bold">{jogador.pomodoros}</span></p>
              <p className="text-sm">⚔️ Cimitarras: <span className="text-blue-400 font-bold">{jogador.cimitarras}</span></p>
            </div>
          </div>

          <div className="bg-gray-800 rounded-lg p-4">
            <div className="flex items-center mb-2">
              <Crown className="w-5 h-5 mr-2 text-purple-400" />
              <h3 className="text-lg font-bold">Semana {semana}</h3>
            </div>
            <p className="text-sm text-gray-300">Boss da Semana:</p>
            <p className="text-sm font-bold text-yellow-400">{bossAtualData.disciplina}</p>
          </div>
        </div>

        {/* Boss Atual */}
        <div className="bg-gray-800 rounded-lg p-6 mb-6">
          <div className="text-center mb-4">
            {/* Avatar do Boss */}
            {bossAtualData.imagem && (
              <div className="w-32 h-32 mx-auto mb-4 rounded-lg overflow-hidden bg-gradient-to-br from-yellow-600 to-orange-700 p-1">
                <img 
                  src={bossAtualData.imagem}
                  alt={bossAtualData.nome}
                  className="w-full h-full object-cover rounded-lg"
                  onError={(e) => {
                    e.target.style.display = 'none';
                    e.target.nextSibling.style.display = 'flex';
                  }}
                />
                <div className="w-full h-full bg-gradient-to-br from-yellow-600 to-orange-700 rounded-lg items-center justify-center text-4xl" style={{display: 'none'}}>
                  👑
                </div>
              </div>
            )}
            
            <h2 className="text-2xl font-bold text-yellow-400 mb-2">{bossAtualData.nome}</h2>
            <p className="text-gray-300 mb-2">{bossAtualData.descricao}</p>
            <p className="text-sm text-purple-300">Habilidade Especial: {bossAtualData.habilidade}</p>
          </div>
          
          <div className="mb-4">
            <div className="flex justify-between items-center mb-2">
              <span className="text-sm font-bold">Vida do Boss</span>
              <span className="text-sm">{bossAtualData.vidaAtual} / {bossAtualData.vida}</span>
            </div>
            <div className="w-full bg-gray-700 rounded-full h-4">
              <div 
                className={`${bossAtualData.cor} h-4 rounded-full transition-all duration-500`}
                style={{ width: `${(bossAtualData.vidaAtual / bossAtualData.vida) * 100}%` }}
              ></div>
            </div>
          </div>

          {/* Botões de Ataque */}
          <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
            <button 
              onClick={atacarComPomodoro}
              disabled={jogador.pomodoros <= 0}
              className="bg-red-600 hover:bg-red-700 disabled:bg-gray-600 disabled:cursor-not-allowed p-3 rounded-lg font-bold transition-colors"
            >
              🍅 Atacar com {jogador.equipamentos.pomodoro} ({equipPomodoroAtual.dano} dano)
            </button>
            <button 
              onClick={atacarComCimitarra}
              disabled={jogador.cimitarras <= 0}
              className="bg-blue-600 hover:bg-blue-700 disabled:bg-gray-600 disabled:cursor-not-allowed p-3 rounded-lg font-bold transition-colors"
            >
              ⚔️ Atacar com {jogador.equipamentos.cimitarra} ({equipCimitarraAtual.dano} dano)
            </button>
          </div>
        </div>

        {/* Missões Diárias */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
          <div className="bg-gray-800 rounded-lg p-6">
            <div className="flex items-center mb-4">
              <Clock className="w-5 h-5 mr-2 text-red-400" />
              <h3 className="text-xl font-bold">Estudos (Pomodoros)</h3>
            </div>
            <p className="text-sm text-gray-300 mb-4">Meta diária: 4 x 50 minutos de estudo</p>
            <div className="mb-4">
              <div className="flex justify-between mb-2">
                <span>Progresso: {progressoDiario.pomodoros}/4</span>
                <span className={progressoDiario.metaPomodorosAtingida ? "text-green-400" : "text-yellow-400"}>
                  {progressoDiario.metaPomodorosAtingida ? "✅ Concluído!" : "🎯 Em Progresso"}
                </span>
              </div>
              <div className="w-full bg-gray-700 rounded-full h-3">
                <div 
                  className="bg-red-500 h-3 rounded-full transition-all"
                  style={{ width: `${(progressoDiario.pomodoros / 4) * 100}%` }}
                ></div>
              </div>
            </div>
            <button 
              onClick={adicionarPomodoro}
              className="w-full bg-red-600 hover:bg-red-700 p-2 rounded-lg font-bold transition-colors"
            >
              + Completar 50min de Estudo
            </button>
          </div>

          <div className="bg-gray-800 rounded-lg p-6">
            <div className="flex items-center mb-4">
              <Scroll className="w-5 h-5 mr-2 text-blue-400" />
              <h3 className="text-xl font-bold">Questões (QCs)</h3>
            </div>
            <p className="text-sm text-gray-300 mb-4">Meta diária: 20 questões respondidas</p>
            <div className="mb-4">
              <div className="flex justify-between mb-2">
                <span>Progresso: {progressoDiario.questoes}/20</span>
                <span className={progressoDiario.metaQuestoesAtingida ? "text-green-400" : "text-yellow-400"}>
                  {progressoDiario.metaQuestoesAtingida ? "✅ Concluído!" : "🎯 Em Progresso"}
                </span>
              </div>
              <div className="w-full bg-gray-700 rounded-full h-3">
                <div 
                  className="bg-blue-500 h-3 rounded-full transition-all"
                  style={{ width: `${(progressoDiario.questoes / 20) * 100}%` }}
                ></div>
              </div>
            </div>
            <button 
              onClick={adicionarCimitarra}
              className="w-full bg-blue-600 hover:bg-blue-700 p-2 rounded-lg font-bold transition-colors"
            >
              + Responder 10 Questões
            </button>
          </div>
        </div>

        {/* Equipamentos */}
        <div className="bg-gray-800 rounded-lg p-6 mb-6">
          <div className="flex items-center mb-4">
            <Shield className="w-5 h-5 mr-2 text-purple-400" />
            <h3 className="text-xl font-bold">Equipamentos Atuais</h3>
          </div>
          <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
            <div className="bg-gray-700 p-4 rounded-lg">
              <h4 className="font-bold text-red-400 mb-2">🍅 {jogador.equipamentos.pomodoro}</h4>
              <p className="text-sm text-gray-300">Dano: {equipPomodoroAtual.dano}</p>
              <p className="text-sm text-gray-300">Nível necessário: {equipPomodoroAtual.nivel}</p>
            </div>
            <div className="bg-gray-700 p-4 rounded-lg">
              <h4 className="font-bold text-blue-400 mb-2">⚔️ {jogador.equipamentos.cimitarra}</h4>
              <p className="text-sm text-gray-300">Dano: {equipCimitarraAtual.dano}</p>
              <p className="text-sm text-gray-300">Nível necessário: {equipCimitarraAtual.nivel}</p>
            </div>
          </div>
        </div>

        {/* Conquistas */}
        {jogador.conquistas.length > 0 && (
          <div className="bg-gray-800 rounded-lg p-6 mb-6">
            <div className="flex items-center mb-4">
              <Trophy className="w-5 h-5 mr-2 text-yellow-400" />
              <h3 className="text-xl font-bold">Conquistas</h3>
            </div>
            <div className="grid grid-cols-1 md:grid-cols-2 gap-2">
              {jogador.conquistas.map((conquista, index) => (
                <div key={index} className="bg-yellow-900/30 p-2 rounded text-sm">
                  🏆 {conquista}
                </div>
              ))}
            </div>
          </div>
        )}

        {/* Botões de Controle */}
        <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
          <button 
            onClick={resetDiario}
            className="bg-purple-600 hover:bg-purple-700 p-3 rounded-lg font-bold transition-colors"
          >
            🔄 Reset Diário
          </button>
          <button 
            onClick={proximoBoss}
            className="bg-orange-600 hover:bg-orange-700 p-3 rounded-lg font-bold transition-colors"
          >
            ⏭️ Próximo Boss
          </button>
          <button 
            onClick={() => setJogador(prev => ({ ...prev, xp: prev.xp + 1000 }))}
            className="bg-green-600 hover:bg-green-700 p-3 rounded-lg font-bold transition-colors"
          >
            🎁 XP Bônus (Teste)
          </button>
        </div>

        {/* Lista de Bosses */}
        <div className="mt-8 bg-gray-800 rounded-lg p-6">
          <h3 className="text-xl font-bold mb-4 text-center">📋 Cronograma de Bosses (17 Disciplinas)</h3>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-3">
            {bosses.map((boss, index) => (
              <div 
                key={index} 
                className={`p-3 rounded-lg transition-all ${index === bossAtual ? 'bg-yellow-900/50 border-2 border-yellow-400 transform scale-105' : 'bg-gray-700 hover:bg-gray-600'}`}
              >
                {/* Imagem do Boss */}
                {boss.imagem && (
                  <div className="w-16 h-16 mx-auto mb-2 rounded-lg overflow-hidden">
                    <img 
                      src={boss.imagem}
                      alt={boss.nome}
                      className="w-full h-full object-cover"
                      onError={(e) => {
                        e.target.style.display = 'none';
                        e.target.nextSibling.style.display = 'flex';
                      }}
                    />
                    <div className="w-full h-full bg-gradient-to-br from-gray-600 to-gray-800 rounded-lg items-center justify-center text-lg" style={{display: 'none'}}>
                      👑
                    </div>
                  </div>
                )}
                
                <p className="font-bold text-sm text-center">{boss.disciplina}</p>
                <p className="text-xs text-gray-300 text-center">{boss.nome}</p>
                {index === bossAtual && <p className="text-xs text-yellow-400 mt-1 text-center">👑 Boss Atual</p>}
              </div>
            ))}
          </div>
        </div>
      </div>
    </div>
  );
};

export default MagistraturaRPG;
