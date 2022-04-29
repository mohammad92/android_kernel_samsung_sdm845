dtb-$(CONFIG_SEC_STARQLTE_PROJECT) += sdm845-sec-starqlte-r00.dtb	\
			sdm845-sec-starqlte-r01.dtb			\
			sdm845-sec-starqlte-r02.dtb			\
			sdm845-sec-starqlte-r03.dtb			\
			sdm845-sec-starqlte-r04.dtb			\
			sdm845-sec-starqlte-r05.dtb			\
			sdm845-sec-starqlte-r06.dtb			\
			sdm845-sec-starqlte-r07.dtb			\
			sdm845-sec-starqlte-r08.dtb			\
			sdm845-sec-starqlte-r09.dtb			\
			sdm845-sec-starqlte-r10.dtb			\
			sdm845-sec-starqlte-r11.dtb			\
			sdm845-sec-starqlte-r12.dtb			\
			sdm845-sec-starqlte-r12_v2.1.dtb		\
			sdm845-sec-starqlte-r13.dtb			\
			sdm845-sec-starqlte-r14.dtb

dtb-$(CONFIG_SEC_STAR2QLTE_PROJECT) += sdm845-sec-star2qlte-r00.dtb	\
			sdm845-sec-star2qlte-r01.dtb			\
			sdm845-sec-star2qlte-r02.dtb			\
			sdm845-sec-star2qlte-r03.dtb			\
			sdm845-sec-star2qlte-r04.dtb			\
			sdm845-sec-star2qlte-r05.dtb			\
			sdm845-sec-star2qlte-r06.dtb			\
			sdm845-sec-star2qlte-r07.dtb			\
			sdm845-sec-star2qlte-r08.dtb			\
			sdm845-sec-star2qlte-r09.dtb			\
			sdm845-sec-star2qlte-r10.dtb			\
			sdm845-sec-star2qlte-r11.dtb			\
			sdm845-sec-star2qlte-r12.dtb			\
			sdm845-sec-star2qlte-r12_v2.1.dtb		\
			sdm845-sec-star2qlte-r13.dtb			\
			sdm845-sec-star2qlte-r14.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../,$(dtb-y))
endif
clean-files := *.dtb *.reverse.dts

