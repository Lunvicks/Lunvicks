-- 👩‍💻 Perfil Profissional | Vitória

WITH perfil_profissional AS (
    SELECT
        'Vitória'                         AS nome,
        'Em transição para Análise de Dados' AS status_carreira,
        'Área de Dados'                   AS area_interesse,
        ARRAY['SQL','Excel','Power BI']   AS habilidades_em_desenvolvimento,
        ARRAY['Análise de Dados','Automação','Indicadores'] AS foco_principal,
        'Gerar insights e apoiar decisões estratégicas' AS objetivo
),

experiencia_atual AS (
    SELECT
        'Atendimento / Cobrança' AS area_atual,
        'Negociação com clientes e foco em metas operacionais' AS atividades,
        ARRAY['Comunicação','Análise de cenário','Resolução de problemas'] AS soft_skills
),

evolucao_profissional AS (
    SELECT
        'Estudos contínuos em dados 📊' AS aprendizado,
        'Desenvolvimento de projetos práticos' AS pratica,
        'Buscando oportunidade na área de dados 🚀' AS proximo_passo
)

SELECT
    p.nome,
    p.status_carreira,
    p.area_interesse,
    p.habilidades_em_desenvolvimento,
    p.foco_principal,
    e.area_atual,
    e.atividades,
    e.soft_skills,
    ev.aprendizado,
    ev.pratica,
    ev.proximo_passo,
    p.objetivo
FROM perfil_profissional p
CROSS JOIN experiencia_atual e
CROSS JOIN evolucao_profissional ev;