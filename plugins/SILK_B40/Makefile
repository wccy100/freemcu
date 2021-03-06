AC_PLUGIN_DIR=codecs/audio
prefix=/opt/freemcu/lib/ptlib
target_os=linux-gnu

SONAME	= silk_b40

SRCDIR	= ./silkSrc
OBJDIR	= ./obj
PLUGINDIR=../..

CC		=gcc
CXX		=g++
LDSO		=-shared -Wl,-soname,$(SONAME)
PLUGINEXT	=so
CFLAGS	       +=-g  -Os
STDCCFLAGS	=-fPIC -D__STDC_CONSTANT_MACROS
LDFLAGS	       +=
EXTRACFLAGS     =-I$(PLUGINDIR)

SRCS = silkcodec.cxx \
SKP_Silk_A2NLSF.c \
SKP_Silk_CNG.c \
SKP_Silk_HP_variable_cutoff_FIX.c \
SKP_Silk_LBRR_reset.c \
SKP_Silk_LPC_inv_pred_gain.c \
SKP_Silk_LPC_synthesis_filter.c \
SKP_Silk_LPC_synthesis_order16.c \
SKP_Silk_LP_variable_cutoff.c \
SKP_Silk_LSF_cos_table.c \
SKP_Silk_LTP_analysis_filter_FIX.c \
SKP_Silk_LTP_scale_ctrl_FIX.c \
SKP_Silk_MA.c \
SKP_Silk_NLSF2A.c \
SKP_Silk_NLSF2A_stable.c \
SKP_Silk_NLSF_MSVQ_decode.c \
SKP_Silk_NLSF_MSVQ_encode_FIX.c \
SKP_Silk_NLSF_VQ_rate_distortion_FIX.c \
SKP_Silk_NLSF_VQ_sum_error_FIX.c \
SKP_Silk_NLSF_VQ_weights_laroia.c \
SKP_Silk_NLSF_stabilize.c \
SKP_Silk_NSQ.c \
SKP_Silk_NSQ_del_dec.c \
SKP_Silk_PLC.c \
SKP_Silk_VAD.c \
SKP_Silk_VQ_nearest_neighbor_FIX.c \
SKP_Silk_ana_filt_bank_1.c \
SKP_Silk_apply_sine_window_new.c \
SKP_Silk_array_maxabs.c \
SKP_Silk_autocorr.c \
SKP_Silk_biquad.c \
SKP_Silk_biquad_alt.c \
SKP_Silk_burg_modified.c \
SKP_Silk_bwexpander.c \
SKP_Silk_bwexpander_32.c \
SKP_Silk_code_signs.c \
SKP_Silk_control_audio_bandwidth.c \
SKP_Silk_control_codec_FIX.c \
SKP_Silk_corrMatrix_FIX.c \
SKP_Silk_create_init_destroy.c \
SKP_Silk_dec_API.c \
SKP_Silk_decode_core.c \
SKP_Silk_decode_frame.c \
SKP_Silk_decode_parameters.c \
SKP_Silk_decode_pitch.c \
SKP_Silk_decode_pulses.c \
SKP_Silk_decoder_set_fs.c \
SKP_Silk_detect_SWB_input.c \
SKP_Silk_enc_API.c \
SKP_Silk_encode_frame_FIX.c \
SKP_Silk_encode_parameters.c \
SKP_Silk_encode_pulses.c \
SKP_Silk_find_LPC_FIX.c \
SKP_Silk_find_LTP_FIX.c \
SKP_Silk_find_pitch_lags_FIX.c \
SKP_Silk_find_pred_coefs_FIX.c \
SKP_Silk_gain_quant.c \
SKP_Silk_init_encoder_FIX.c \
SKP_Silk_inner_prod_aligned.c \
SKP_Silk_interpolate.c \
SKP_Silk_k2a.c \
SKP_Silk_k2a_Q16.c \
SKP_Silk_lin2log.c \
SKP_Silk_log2lin.c \
SKP_Silk_noise_shape_analysis_FIX.c \
SKP_Silk_pitch_analysis_core.c \
SKP_Silk_pitch_est_tables.c \
SKP_Silk_prefilter_FIX.c \
SKP_Silk_process_NLSFs_FIX.c \
SKP_Silk_process_gains_FIX.c \
SKP_Silk_quant_LTP_gains_FIX.c \
SKP_Silk_range_coder.c \
SKP_Silk_regularize_correlations_FIX.c \
SKP_Silk_resampler.c \
SKP_Silk_resampler_down2.c \
SKP_Silk_resampler_down2_3.c \
SKP_Silk_resampler_down3.c \
SKP_Silk_resampler_private_AR2.c \
SKP_Silk_resampler_private_ARMA4.c \
SKP_Silk_resampler_private_IIR_FIR.c \
SKP_Silk_resampler_private_copy.c \
SKP_Silk_resampler_private_down4.c \
SKP_Silk_resampler_private_down_FIR.c \
SKP_Silk_resampler_private_up2_HQ.c \
SKP_Silk_resampler_private_up4.c \
SKP_Silk_resampler_rom.c \
SKP_Silk_resampler_up2.c \
SKP_Silk_residual_energy16_FIX.c \
SKP_Silk_residual_energy_FIX.c \
SKP_Silk_scale_copy_vector16.c \
SKP_Silk_scale_vector.c \
SKP_Silk_schur.c \
SKP_Silk_schur64.c \
SKP_Silk_shell_coder.c \
SKP_Silk_sigm_Q15.c \
SKP_Silk_solve_LS_FIX.c \
SKP_Silk_sort.c \
SKP_Silk_sum_sqr_shift.c \
SKP_Silk_tables_LTP.c \
SKP_Silk_tables_NLSF_CB0_10.c \
SKP_Silk_tables_NLSF_CB0_16.c \
SKP_Silk_tables_NLSF_CB1_10.c \
SKP_Silk_tables_NLSF_CB1_16.c \
SKP_Silk_tables_gain.c \
SKP_Silk_tables_other.c \
SKP_Silk_tables_pitch_lag.c \
SKP_Silk_tables_pulses_per_block.c \
SKP_Silk_tables_sign.c \
SKP_Silk_tables_type_offset.c \
SKP_Silk_warped_autocorrelation_FIX.c 

vpath	%.o $(OBJDIR)
vpath	%.c $(SRCDIR)
vpath	%.cxx .

ifeq ($(VERBOSE),)
Q_CC = @echo [CC] `echo $< | sed s^@OPALDIR@/^^` ;
Q_LD = @echo [LD] `echo $(PLUGIN) | sed s^@OPALDIR@/^^` ;
endif


$(OBJDIR)/%.o : %.c
	@mkdir -p $(OBJDIR) >/dev/null 2>&1
	$(Q_CC)$(CC) -I../../../include $(STDCCFLAGS) $(OPTCCFLAGS) $(EXTRACFLAGS) $(CFLAGS) -c $< -o $@

$(OBJDIR)/%.o : %.cxx
	@mkdir -p $(OBJDIR) >/dev/null 2>&1
	$(CXX) $(EXTRACCFLAGS) $(STDCCFLAGS) $(OPTCCFLAGS) $(CFLAGS) -c $< -o $@

PLUGIN	= ./silk_b40_audio_pwplugin.$(PLUGINEXT)

OBJECTS = $(addprefix $(OBJDIR)/,$(patsubst %.c,%.o,$(patsubst %.cxx,%.o,$(notdir $(SRCS)))))

all: $(PLUGIN)

$(PLUGIN): $(OBJECTS)
ifeq (solaris,$(findstring solaris,$(target_os)))

	$(Q_LD)$(CXX) $(LDSO) $@ -o $@ $^ $(EXTRALIBS)
else
	$(Q_LD)$(CXX) $(LDSO) -o $@ $^ $(EXTRALIBS)

endif	

install:
	mkdir -p $(DESTDIR)$(prefix)/$(AC_PLUGIN_DIR)
	install $(PLUGIN) $(DESTDIR)$(prefix)/$(AC_PLUGIN_DIR)

uninstall:
	rm -f $(DESTDIR)$(prefix)/$(AC_PLUGIN_DIR)/$(PLUGIN)

clean:
	rm -f $(OBJECTS) $(PLUGIN)

###########################################

