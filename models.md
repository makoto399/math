$\epsilon_t, \delta_t, v_t, w_t, \eta_t$は特段断りがない場合は互いに独立な正規分布などの任意の分布に従う確率変数
| モデル名                   | 数式（TeX表記）                                                                                                                   | 説明                                           |  パラメータ推定                                                | シミュレーション負荷                               |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ------------------------------------------------ | ------------------------------ |
| **AR(OU)**           | $r_t = \theta(\mu - r_{t-1} ) + \epsilon_t $                                                                                     | 過去の値からの自己回帰。基本モデル。                           |                                                  |                                |
| **Additive Jump AR**           | $r_t = \theta(\mu - r_{t-1} ) + \epsilon_t + \delta^U_t I^U_t + \delta^D_t I^D_t \\ I^U_t 〜 {\rm Bern(\lambda^U)} \\ I^D_t 〜 {\rm Bern(\lambda^D)} $                                                                                   | 過去の値からの自己回帰。基本モデル。                           |                                                  |                                |
| **State-dependent Jump AR**           | $r_t = 1_{\{I^U_t=0 \land I^D_t=0\}} \left\{ \theta(\mu - r_{t-1} ) + \epsilon_t \right\} + \delta^U_t I^U_t + \delta^D_t I^D_t　\\ I^U_t 〜 {\rm Bern(\lambda^U)} \\ I^D_t 〜 {\rm Bern(\lambda^D)}$                                                                           | 過去の値からの自己回帰。基本モデル。                           |                                                  |                                |
| **MA**           | $r_t = \mu + \epsilon_t + \psi \epsilon_{t-1}$                                                                          | 過去の誤差（ショック）からの影響。                            |                                                  |                                |
| **ARIMA**              | $\Delta r_t = \theta(\mu - \Delta r_{t-1}) + \epsilon_t + \psi \epsilon_{t-1}$                                                                                     | 非定常系列に対応（差分化 + ARMA）。                        |                                                  |                                |
| **ARCH**               | $r_t = \mu + \epsilon_t , \epsilon_t〜N(0,\sqrt{h_t})\\ h_t = \alpha_0 + \alpha_1 \epsilon_{t-1}^2$                                                                         | 分散が過去の誤差に依存（分散の条件付きモデル）。                     |                                                  |                                |
| **GARCH**              | $r_t = \mu + \epsilon_t, \epsilon_t〜N(0,\sqrt{h_t}) \\ h_t = \omega + \alpha \epsilon_{t-1}^2 + \beta h_{t-1}$                                                      | 分散の自己回帰も導入。長期的なボラティリティを表現。                   |                                                  |                                |
| **EGARCH**             | $r_t = \mu + \epsilon_t, \epsilon_t〜N(0,\sqrt{h_t}) \\ \log(h_t) = \omega + \beta \log(h_{t-1}) + \alpha {\|} \frac{\epsilon_{t-1}}{\sqrt{h_{t-1}}} {\|} + \gamma \frac{\epsilon_{t-1}}{\sqrt{h_{t-1}}}$| 負のショックと正のショックの影響を区別可能。レバレッジ効果。 |
| **TGARCH(GJR-GARCH)** | $r_t = \mu + \epsilon_t, \epsilon_t〜N(0,\sqrt{h_t}) \\ h_t = \omega + \alpha \epsilon_{t-1}^2 + \gamma \epsilon_{t-1}^2 1_{\{\epsilon_{t-1} < 0\}} + \beta h_t$ | TGARCHは負のショックでより大きな分散変化（非対称性）を表現。            |                                                  |                                |
| **Regime Switching**   | $r_t = \mu_{s_t} + \phi_{s_t} r_{t-1} + \epsilon_t, \quad s_t \sim \text{MC(P)}$                                   | マルコフ過程で状態転換（構造が変わる時系列）。                      |                                                  |                                |
| **State Space Model**  | $r_t = H x_t + v_t \\ x_t = F x_{t-1} + w_t $                                                    | 観測されない状態変数を含み、カルマンフィルタなどで推定。                 |                                                  |                                |
| **SV** | $r_t = \exp(h_t/2)\epsilon_t \\ h_t = \alpha + \beta h_{t-1} + \eta_t$ |    |                                                  |                                |

- パラメータ推定
  - 期間は長め（パラメータも多めなので。経験上は1パラメータあたり100は欲しい）
  - 2022年度と2023年度初期はフラグ立てする
- 先物との整合性

- 現モデルの評価
  - バックテスト
    - 2023年度までで推定し
      - 2024年度の結果は分布の中に入っているか
      - 時系列クラスタリングは近しいか
  - 運用上の評価
    -  2023年度までで推定した結果と全期間で推定した結果で
       -  パラメータは大きく変化しないか
       -  向こう１年後、５年後の分布に大きな変化はないか
    -  パラメータ推定時間
    -  シミュレーションまでの時間
- 新モデルの評価
   - 個別に以下を評価した上で、全体で俯瞰してみたときに、最も良いモデルを選ぶ（モデルの切り替えは考えていない）
     - バックテスト
        - 同じ
        - RMSEは小さいか
     -  運用上の評価
        -  同じ
     -  その他
        -  将来シミュレーション結果は分布が狭すぎないか？
