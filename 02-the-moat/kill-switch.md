# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** |اعتماد محتمل/جزئي على مزود واحد (غالبًا OpenAI أو مزود عالمي)| H |تفعيل مزود بديل (Model ثاني / self-hosted) + إعداد credentials جاهزة|
| **Abstraction** |تفعيل مزود بديل (Model ثاني / self-hosted) + إعداد credentials جاهزة | H | إنشاء API موحد داخلي (AI Gateway) وتحويل كل الcalls له|
| **Routing** |لا يوجد dynamic routing بين موديلات | M |تفعيل rule-based routing (fallback model + load split) |
| **Eval** |لا يوجد benchmark موحد لقياس جودة النماذج | H |بناء dataset سريع من قرارات حقيقية + تشغيل مقارنة بين موديلين |

## Portability Score
Score: 6 / 20

## If [primary vendor] doubles pricing tomorrow:
الأثر:

ارتفاع تكلفة التشغيل بشكل مباشر (خصوصًا مع حجم SDP)
ضغط على الميزانيات التشغيلية
تعطّل التوسع في AI

## If [primary vendor] ships a competing product:
<!-- What's defensible that they can't replicate? -->
الأثر:

يقدم:
Decision AI جاهز
Gov Copilot
الجهات تبدأ تعتمد عليه مباشرة
